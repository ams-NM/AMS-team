- {{query (and (task TODO DONE) (property :plan [[2023-07-24 Mon]])  )}}
  query-sort-by:: block
  query-table:: true
  query-sort-desc:: true
  query-properties:: [:block :finish :remark]
- ---
- query-sort-by:: finish
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-24 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-24 Mon")
  ]
  }
  #+END_QUERY