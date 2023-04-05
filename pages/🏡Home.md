public:: true

- ## Events -Ongoing
  collapsed:: true
	- {{query (and [[event]] (property :status "ongoing"))}}
	  query-table:: true
	  query-properties:: [:block :start]
	  query-sort-by:: start
	  query-sort-desc:: false
- ## 🗓️Schedule
  collapsed:: true
	- {{query (and (task TODO DONE) (not [[Templates/monthly]]) (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:plan :block :finished]
	  query-sort-by:: plan
	  query-sort-desc:: false
- ## Calibration Records
  collapsed:: true
	- {{query (and [[cal-due]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :due :out :sn :wo]
- ## PR Pending
  collapsed:: true
	- {{query (and [[pr-pending]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :pr :issued]
- ---
- ## Test query
	- query-table:: false
	  #+BEGIN_QUERY
	  {
	   :title [:b "Block query"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?today
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO", "DONE"})
	           ]
	   :inputs [ :-1d :today ]
	   }
	  #+END_QUERY
- ```Clojure
  {
   :title [:b "Block query"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?today
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO", "DONE"})
           ]
   :inputs [ :-7d :today ]
   }
  ```