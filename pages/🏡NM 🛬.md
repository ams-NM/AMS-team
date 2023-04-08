-
- ## 📌Outstanding
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-table:: true
	  query-properties:: [:plan :block]
- ## Weekly View
	- #{"2023-04-03 Mon", "2023-04-04 Tue", "2023-04-05 Wed", "2023-04-06 Thu", "2023-04-07 Fri", "2023-04-10 Mon"}
	- (or (property :plan "2023-04-10 Mon") (property :plan "2023-04-11 Tue") )
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title "Tasks in last 7 days"
	   :query [:find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           (or [property :plan "2023-04-10 Mon"] [property :plan "2023-04-11 Tue"])
	  ]}
	  #+END_QUERY
- ## 🗓️Schedule
  collapsed:: true
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan))}}
	  query-table:: true
	  query-properties:: [:plan :block :remark]
	  query-sort-by:: plan
	  query-sort-desc:: false
- ## ⏳Calibration Records
  collapsed:: true
	- {{query (and [[cal-due]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :due :out :sn :wo]
- ## 🛒PR Pending
  collapsed:: true
	- {{query (and [[pr-pending]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :pr :issued]
-
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