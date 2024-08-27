filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w25]]) << | >> [Next Week]([[Weekly/2023 w27]])
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-26 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-26 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-27 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-27 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-28 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-28 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-29 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-29 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-30 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-30 Fri")
  ]}
  #+END_QUERY