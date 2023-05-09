-
- ## 📌Outstanding
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-table:: true
	  query-properties:: [:plan :block]
	  query-sort-by:: plan
	  query-sort-desc:: false
- ## 7️⃣Weekly Viewtw
	- [[Weekly]]
	- [[Weekly/2023 w19]]
	- [[Weekly/2023 w20]]
	- [[Weekly/2023 w21]]
	- [[Weekly/2023 w22]]
- ## 🗓️Schedule
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan)) )}}
	  query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block :finished :remark]
- ## 🏋️CWOs -[[CWO -ALL]]
  collapsed:: true
	- {{query (and [[CWO -ALL]] (not [[Templates/misc]] ) #cwo (property :status "ongoing") )}}
	  query-table:: true
	  query-properties:: [:block :wo :remark]
- ## ⏳[[Calibration]] - [[AWOS]]
  collapsed:: true
	- {{query (and (or [[Calibration/HMP]] [[Calibration/PTB]] ) [[cal-due]] (not [[Templates/misc]]))}}
	  query-sort-by:: due
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :due :out :sn :wo :remark]
- ## 🛒PR Pending
  collapsed:: true
	- {{query (and [[PR-pending]] (not [[Vault]] ) (not [[Templates/misc]]))}}
	  query-sort-by:: issued
	  query-table:: true
	  query-sort-desc:: true
	  query-properties:: [:block :issued :pr :wo]
- ## [[Vault]]
- ---
-
- ## Test query
  collapsed:: true
	- ```Clojure
	  {
	   :title [:b "Block query"]
	   :query [
	           :find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO", "DONE"})
	           (property ?b :plan "2023-04-10 Mon")
	           ]
	   }
	  ```
	- query-table:: true
	  collapsed:: true
	  #+BEGIN_QUERY
	  {
	   :title [:h2 "Block query"]
	   :query [
	           :find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           (property ?b :plan "2023-04-10 Mon")
	           ]
	   }
	  #+END_QUERY
	- collapsed:: true