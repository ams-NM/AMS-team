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
	- {{query (and [[pr-pending]] (not [[Templates/misc]]))}}
	  query-table:: true
	  query-properties:: [:block :pr :issued]
- ## Test query
	- #+BEGIN_QUERY
	  
	  #+END_QUERY
- ```Clojure
  {
   :title [:b "query"]
   :query [
           
           ]
   }
  ```