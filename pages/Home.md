filters:: {"🏠nm tasks & schedule" false}
icon:: 🏡

- [[🏠NM Tasks & Schedule]]
- ## ⏰TODAY
	- query-table:: true
	  query-properties:: [:block :date :remark]
	  #+BEGIN_QUERY
	  {
	   :title [:h4 "🥵TODO"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           (task ?b #{"TODO"})
	           [?pt :block/name "personal"]
	           [?b :block/refs ?p]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:-1m :today]
	   }
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  query-sort-by:: block
	  query-sort-desc:: false
	  #+BEGIN_QUERY
	  {
	   :title [:h4 "✔️DONE"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           (task ?b #{"DONE"})
	           [?b :block/refs ?p]
	           [?b :block/path-refs [:block/name "personal"]]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:today :today]
	   }
	  #+END_QUERY
- ## TODOs
-
- [[Test Page]]
- query-table:: true
  query-properties:: [:block :date]
- query-sort-by:: date
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "🗓️My Errands for Next 30 days"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           [?b :block/path-refs [:block/name "personal"]]
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(>= ?dnum ?start)]
           [(<= ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:today :+30d]
   }
  #+END_QUERY