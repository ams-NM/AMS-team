public:: true

- ## Today
	- {{query (and (and (task DONE TODO) (property :plan [[2023-04-05 Wed]] )) (not [[Templates/misc]]) (not [[Templates/monthly]]))}}
	  query-table:: true
- ## Schedule
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
	  query-properties:: [:block :pr-no :issued :received]