filters:: {"weekly" false}

- [Last Week]([[Weekly/2025 w13]]) << | >> [Next Week]([[Weekly/2025 w15]])
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-03-31 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-03-31 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-04-01 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-04-01 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-04-02 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-04-02 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-04-03 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-04-03 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2025-04-04 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2025-04-04 Fri")
  ]}
  #+END_QUERY