filters:: {"weekly" false}

- [Last Week]([[Weekly/2025 w09]]) << | >> [Next Week]([[Weekly/2025 w11]])
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-03 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-03 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-04 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-04 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-05 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-05 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-06 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-06 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-07 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-07 Fri")
  ]}
  #+END_QUERY