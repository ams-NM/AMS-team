- Press ==tw== to toggle full page width.
- ## 📌Outstanding
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block]
- ## 7️⃣Weekly View
  collapsed:: true
	- [[Weekly]]
	-
	- [[Weekly/2023 w20]]
	- [[Weekly/2023 w21]]
	- [[Weekly/2023 w22]]
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
	- {{query (and [[CWO -ALL]] (not [[Templates/misc]] ) #cwo (property :status "ongoing") )}}
	  query-table:: true
	  query-properties:: [:block :wo :remark]
- ## ⏳[[Calibration]] - [[AWOS]]
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