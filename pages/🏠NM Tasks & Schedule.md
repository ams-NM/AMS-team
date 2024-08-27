- Press ==tw== keys to toggle page width.
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  query-sort-by:: block
  query-sort-desc:: false
  collapsed:: true
  #+BEGIN_QUERY
  {
  :title [:H2 "📌Outstanding"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "outstanding"]
           [?b :block/refs ?p]]}
  #+END_QUERY
- ## 7️⃣ [[Weekly]] View
	- [[Weekly/2024 w36]]
	- [[Weekly/2024 w37]]
- ## 🗓️Schedule
	- query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block :remark]
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
- ## 🏋️CWO Ongoing
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
	- Live query: `{{query (and [[Calibration/HMP]] #cal-due )}}`
	- Live query: `{{query (and [[Calibration/PTB]] #cal-due )}}`
	- query-sort-by:: due
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :due :out :sn :remark]
	  #+BEGIN_QUERY
	  {:title [:H3 "HMP"]
	   :query [:find (pull ?b [*])
	       :where
	       [?p :block/name "cal-due"]
	       [?b :block/path-refs [:block/name "calibration/hmp"]]
	       (not [?b :block/path-refs [:block/name "templates/misc"]])
	       (not [?b :block/path-refs [:block/name "workflows"]])
	       ]}
	  #+END_QUERY
	-
	- query-sort-by:: due
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :due :out :sn :remark]
	  #+BEGIN_QUERY
	  {:title [:H3 "PTB"]
	   :query [:find (pull ?b [*])
	       :where
	       [?p :block/name "cal-due"]
	       [?b :block/path-refs [:block/name "calibration/ptb"]]
	       (not [?b :block/path-refs [:block/name "templates/misc"]])
	       (not [?b :block/path-refs [:block/name "workflows"]])
	       ]}
	  #+END_QUERY
	-
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
  query-properties:: [:block :wo :issued]
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
	- {{query (and [[Calibration/HMP]] #cal-due )}}
	  query-table:: true
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