query-sort-by:: block
query-table:: true
query-sort-desc:: false
query-properties:: [:block :finish :remark]

- :inputs ["[[2024-09-01 Sun]]" "[[2024-09-30 Mon]]"]
- ## Query Labor Data
	- query-table:: true
	  query-properties:: [:block :date :time :wo :staffs]
	  #+BEGIN_QUERY
	  {
	   :title [:h3 "Labor Data of The Month"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           [?p :block/name "labor-todo"]
	           [?b :block/refs ?p]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:-30d :today]
	   }
	  #+END_QUERY
- ## Test data
	- TODO==Test==  [[ILS]] Weekly, 📄Monitor Printouts 
	  tags:: labor-todo
	  date:: [[2024-09-01 Sun]]
	  time:: 14:00-18:00
	  wo:: 647315
	  staffs:: [[ALL]]
	- DONE `W01` [[ILS]] Weekly ,  🏠️Site Visit
	  tags:: labor-todo
	  date:: [[2024-09-04 Wed]]
	  time:: 09:00-13:00
	  wo:: 647315
	  staffs:: [[Nick]]
- ---
- ## [[Maximo]] ==Labor== -2024-09
  query-sort-by:: due
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:finish :block :due :out :sn :location :remark]
	- | Staff   |  Hours |   Start Date        |  Start Time | End Date | End Time | WO | Description |
	  |----------:|-------------:|------:|----------:|-------------:|------:|
	  |  All - [[Vincent]] | | 09-16  | 09  |   |  13 |  647315  |  ILS weekly |
	  | [[Vincent]] | 8|   09-16 |   |   |   |  TRAIN  |   |
	  |   |    |   |   |   |    |   |    |
	  |   |    |   |   |   |    |   |    |
	-
-