- {{renderer :kanban_owjgujpm}}
	- tasks
		- #+BEGIN_QUERY
		  {
		   :query [
		           :find (pull ?b [*])
		           :where
		          (?b :block/page ?page)
		          (not (?p "Templates/pm-tasks"))
		          (task ?b #{"TODO" "DOING" "DONE"})
		          
		           ] 
		   }
		  #+END_QUERY
	- {{query (and (task TODO) (not [[Templates/pm-tasks]]) (not [[Templates/monthly]]) (not [[Templates/misc]]) (property :plan))}}
	  query-table:: false
	  query-sort-by:: plan
	  query-sort-desc:: false
	  collapsed:: true
-
	- Pending
		- ((64336b8e-cbbc-4936-9eaa-81319c456bda))
	- Planed
		- ((64336b8e-01de-4953-b9c0-3f9f716ca3d0))
	- Done
		- ((64336b8e-a294-4a9a-9e28-fea5c609236a))
	-
	-
-