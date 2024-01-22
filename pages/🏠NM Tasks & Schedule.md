- Press ==tw== to toggle full page width.
- query-table:: true
  query-properties:: [:block :plan :finished :remark]
  #+BEGIN_QUERY
  {
  :title [:H2 "📌Outstanding"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "outstanding"]
           [?b :block/refs ?p]]}
  #+END_QUERY
- ## 7️⃣Weekly View
  collapsed:: true
	- [[Weekly]]
	-
	- [[Weekly/2023 w28]]
	- [[Weekly/2023 w29]]
	- [[Weekly/2023 w30]]
	- [[Weekly/2023 w31]]
- ## 🗓️Schedule
  collapsed:: true
	- query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block :finished :remark]
	  #+BEGIN_QUERY
	  {
	   :title [:h3 "Tasks and Events"]
	   :query [
	           :find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO"})
	           [?b :block/properties ?pros]
	           [(get ?pros :plan) ?bn]
	           (not [(= ?bn "")])
	           ]
	   }
	  #+END_QUERY
- collapsed:: true
  #+BEGIN_QUERY
  {:title [:H2 "🏋️CWO Ongoing"]
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
	- #+BEGIN_QUERY
	  {:title []
	   :query [:find (pull ?b [*])
	       :where
	       [?b :block/marker ?marker]
	       [?b :block/path-refs [:block/name "calibration/hmp"]]
	       ([?b :block/path-refs [:block/name "calibration/hmp"]])
	       ]}
	  #+END_QUERY
	- {{query (and [[Calibration/HMP]] [[cal-due]] (not [[Templates/misc]]))}}
	  query-sort-by:: due
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :due :out :sn :wo :remark]
	- {{query (and [[Calibration/PTB]] [[cal-due]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :due :out :sn :wo :remark]
	  query-sort-by:: due
	  query-sort-desc:: false
- query-table:: true
  query-properties:: [:block :pr :wo :issued]
  collapsed:: true
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
  query-properties:: [:block :tags :wo :issued]
  collapsed:: true
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
- ## [[Vault]]
- ---
- ## Test query
  collapsed:: true
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
	           [(get ?pros :plan) ?bn]
	           (not [(= ?bn "")])
	           ]
	   }
	  #+END_QUERY
	  ```
	- query-sort-by:: block
	  query-table:: true
	  query-sort-desc:: true
	  query-properties:: [:block :plan]
	  ```
	  {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan)) )}}
	  ```
		- query-table:: true
		  query-properties:: [:plan :block :remark]
		  query-sort-by:: plan
		  query-sort-desc:: false
	-