- Press ==tw== keys to toggle page width.
- ==Page updates== at the 10th minute every hour.
- ##
- query-sort-by:: date
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "⏰TODAY"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "personal"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:-1m :today]
   }
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "📌Outstanding"]
   :query [
           :find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO"})
           [?p :block/name "outstanding"]
           [?b :block/refs ?p]
           ]
   }
  #+END_QUERY
- ## 7️⃣ [[Weekly]] View
	- [[Weekly/2024 w38]]
	- [[Weekly/2024 w39]]
	- [[Weekly/2024 w40]]
- query-sort-by:: date
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:date :block :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {
   :title [:h2 "🗓️Schedule for Next 7 days"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "personal"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:+1d :+7d]
   }
  #+END_QUERY
- ## ((66e7b5c6-433f-4493-b3ab-891bc5bc80fc))
- query-table:: true
  query-properties:: [:block :remark]
  #+BEGIN_QUERY
  {
   :title [:h2 "⏳Pending"]
   :query [
           :find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO"})
           [?p :block/name "pending"]
           [?b :block/refs ?p]
           ]
   }
  #+END_QUERY
- ## 🏋️CWO Ongoing
  collapsed:: true
	- query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:H2 "CWO"]
	   :query [:find ?name
	         :in $ ?tag
	         :where
	         (page-property ?p :status "ongoing")
	         [?t :block/name ?tag]
	         [?p :page/tags ?t]
	         [?p :block/name ?name]]
	   :inputs ["cwo"]
	   :view (fn [result]
	         [:div.flex.flex-col
	          (for [page result]
	            [:a {:href (str "#/page/" page)} (clojure.string/capitalize page)])])}
	  #+END_QUERY
- ## ⏳[[Calibration]] - [[AWOS]]
  collapsed:: true
	- ### HMP
		- {{query (and [[Calibration/HMP]] #cal-due )}}
		  query-table:: true
		  query-properties:: [:block :due :out :sn :location :remark]
		  query-sort-by:: due
		  query-sort-desc:: false
	- ### PTB
		- {{query (and [[Calibration/PTB]] #cal-due )}}
		  query-table:: true
		  query-properties:: [:block :due :out :sn :location :remark]
		  query-sort-by:: due
		  query-sort-desc:: false
- query-table:: true
  query-properties:: [:block :pr :wo :issued]
  #+BEGIN_QUERY
  {
  :title [:H2 "🛒PR Pending"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "pr-pending"]
           (not [?b :block/path-refs [:block/name "templates/misc"]])
           [?b :block/refs ?p]
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :wo :issued :remark]
  #+BEGIN_QUERY
  {
  :title [:H2 "🛒IMO Pending"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "imo-pending"]
           (not [?b :block/path-refs [:block/name "templates/misc"]])
           [?b :block/refs ?p]
  ]}
  #+END_QUERY
- query-sort-by:: block
  query-table:: true
  query-sort-desc:: true
  query-properties:: [:block :start :status :complete :tags :issued :wo]
-
- #### [[Home]]
- ---
- ## Test query
  collapsed:: true
	-
	-
		- query-table:: true
		  query-properties:: [:block :date]
		- query-sort-by:: date
		  query-table:: true
		  query-sort-desc:: false
		  query-properties:: [:block :date]
		- query-table:: true
		  query-properties:: [:block :due :out :sn :remark]
		- ```Clojure
		  #+BEGIN_QUERY
		  {
		   :title [:h3 "Schedule"]
		   :query [
		           :find (pull ?b [*])
		           :where
		           [?b :block/parent ?parent]
		           (not (has-property ?parent :template))
		           (task ?b #{"TODO"})
		           [?b :block/properties ?pros]
		           [(get ?pros :date) ?bn]
		           (not [(= ?bn "")])
		           ]
		   }
		  #+END_QUERY
		  ```
		- query-sort-by:: block
		  query-table:: true
		  query-sort-desc:: true
		  query-properties:: [:block :date]
		  collapsed:: true
		  ```
		  {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :date)) )}}
		  ```
			- query-table:: true
			  query-properties:: [:date :block :remark]
			  query-sort-by:: plan
			  query-sort-desc:: false
		-