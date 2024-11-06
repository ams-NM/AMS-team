filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w44]]) << | >> [Next Week]([[Weekly/2024 w46]])
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-11-04 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-11-04 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-11-05 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-11-05 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-11-06 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-11-06 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-11-07 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-11-07 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-11-08 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-11-08 Fri")
  ]}
  #+END_QUERY
-
-