public:: true

- ## Outstanding
	- {{query (and #outstanding (not (property :status "done")))}}
	  query-table:: true
	  query-properties:: [:plan :block]
- ## 🗓️Schedule
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan))}}
	  query-table:: true
	  query-properties:: [:plan :block :remark]
- ## Calibration Records
	- {{query (and [[cal-due]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :due :out :sn :wo]
- ## PR Pending
	- {{query (and [[pr-pending]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :pr :issued]
-
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
	           (property ?b :plan "2023-04-05 Wed")
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
	           (task ?b #{"TODO", "DONE"})
	           (property ?b :plan "2023-04-05 Wed")
	           ]
	   }
	  #+END_QUERY