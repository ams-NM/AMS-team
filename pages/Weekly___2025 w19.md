filters:: {"weekly" false}

- [Last Week]([[Weekly/2025 w18]]) << | >> [Next Week]([[Weekly/2025 w20]])
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-05-05 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-05-05 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-05-06 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-05-06 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-05-07 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-05-07 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-05-08 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-05-08 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-05-09 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-05-09 Fri")
  ]}
  #+END_QUERY