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
- ## 🏋️CWOs -[[CWO -ALL]]
	- {{query (and [[CWO -ALL]] [[cwo]] (not [[Templates/misc]] )  (property :status "ongoing") )}}
	  query-table:: true
	  query-properties:: [:block :wo :remark]
- ## ⏳[[Calibration]] - [[AWOS]]
  collapsed:: true
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
- ## 🛒PR Pending -
	- {{query (and [[PR-pending]] (not [[Vault]] ) (not [[Templates/misc]]))}}
	  query-sort-by:: issued
	  query-table:: true
	  query-sort-desc:: true
	  query-properties:: [:block :issued :pr :wo]
- ## 🛒IMO Pending -
	- {{query (and [[IMO-pending]] (not [[Vault]] ) (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :remark :page]
	  query-sort-by:: plan
	  query-sort-desc:: false
- query-sort-by:: block
  query-table:: true
  query-sort-desc:: true
  query-properties:: [:block :start :status :complete :tags :page]
  #+BEGIN_QUERY
  {
  :title [:H2 "🛒IMO Pending"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "imo-pending"]
           (not [?p :b/name "Templates/misc"])
           [?b :block/refs ?p]]}
  #+END_QUERY
- ## [[Vault]]
- ---
- ## Test query
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