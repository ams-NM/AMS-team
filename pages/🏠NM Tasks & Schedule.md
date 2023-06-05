- Press ==tw== to toggle full page width.
- ## 📌Outstanding
  collapsed:: true
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block]
- ## 7️⃣Weekly View
	- [[Weekly]]
	-
	- [[Weekly/2023 w23]]
	- [[Weekly/2023 w24]]
	- [[Weekly/2023 w25]]
	- [[Weekly/2023 w26]]
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
  collapsed:: true
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
- ## 🛒PR Pending - 0
  collapsed:: true
	- {{query (and [[PR-pending]] (not [[Vault]] ) (not [[Templates/misc]]))}}
	  query-sort-by:: issued
	  query-table:: true
	  query-sort-desc:: true
	  query-properties:: [:block :issued :pr :wo]
- ## 🛒IMO Pending - 2
  collapsed:: true
	- {{query (and [[IMO-pending]] (not [[Vault]] ) (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :remark]
	  query-sort-by:: plan
	  query-sort-desc:: false
	  collapsed:: true
- ## [[Vault]]
- ---
-
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