-
- ## 📌Outstanding
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-table:: true
	  query-properties:: [:plan :block]
- ## 7️⃣Weekly Viewtw
	- [[Weekly]]
	- [[Weekly/2023 w17]]
	- [[Weekly/2023 w18]]
	- [[Weekly/2023 w19]]
- ## 🗓️Schedule
  collapsed:: true
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan)) )}}
	  query-sort-by:: plan
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:plan :block :finished :remark]
- ## [[CWO]]
	- {{query (and [[CWO]] (not [[Templates/misc]] ) #cwo (property :status "ongoing") )}}
	  query-table:: true
	  query-properties:: [:block :wo :start]
- ## ⏳[[Calibration]]
  collapsed:: true
	- {{query (and (or [[Calibration/HMP]] [[Calibration/PTB]] ) [[cal-due]] (not [[Templates/misc]]))}}
	  query-sort-by:: due
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :due :out :sn :wo :remark]
- ## 🛒PR Pending
	- {{query (and [[PR-pending]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :issued :pr :wo]
	  query-sort-by:: issued
	  query-sort-desc:: true
- ## [[Vault]]
- ---
-
- ## Test query
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
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan)) )}}