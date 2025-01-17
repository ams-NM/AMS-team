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
	   :title [:h3 "Labor Data - [[Nick]] "]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end [?staff ...]
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           [?b :block/path-refs [:block/name "labor-todo"]]
	           [?b :block/refs ?p]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(<= ?start ?dnum ?end)]
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           [(contains? ?bn ?jn)]
	           [(get ?properties :staffs) ?stfs]
	           [(contains? ?stfs ?staff)]
	           ]
	  :inputs [20240801 20240830 ["Nick" "All-staffs"]]
	   }
	  #+END_QUERY
- ## Test data
	-
	- DONE ==Test== `W01` [[ILS]] Weekly ,  🏠️Site Visit
	  tags:: labor-todo
	  date:: [[2024-08-04 Sun]]
	  time:: 09:00-13:00
	  wo:: 647315
	  staffs:: [[Nick]]
	- DONE ==Test== `W01` [[ILS]] Weekly ,  🏠️Site Visit
	  tags:: labor-todo
	  date:: [[2024-08-15 Thu]]
	  time:: 09:00-13:00
	  wo:: 647315
	  staffs:: [[Vincent]], [[Eric]]
	-
	- done:: #{"{"}
	- done:: #{"{"}
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