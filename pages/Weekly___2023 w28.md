filters:: {"weekly" false}

- [Last Week]([[Weekly/]]) << | >> [Next Week]([[Weekly/2023 w29]])
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-10 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-10 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-11 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-11 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-12 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-12 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-13 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-13 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-14 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-14 Fri")
  ]}
  #+END_QUERY