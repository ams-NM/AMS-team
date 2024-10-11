filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w42]]) << | >> [Next Week]([[Weekly/2024 w44]])
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-10-14 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-10-14 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-10-15 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-10-15 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-10-16 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-10-16 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-10-17 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-10-17 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-10-18 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-10-18 Fri")
  ]}
  #+END_QUERY
-
-