filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w51]]) << | >> [Next Week]([[Weekly/2025 w01]])
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-12-23 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-12-23 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-12-24 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-12-24 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-12-25 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-12-25 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-12-26 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-12-26 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-12-27 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-12-27 Fri")
  ]}
  #+END_QUERY