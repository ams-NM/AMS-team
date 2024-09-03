filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w34]]) << | >> [Next Week]([[Weekly/2024 w36]])
- query-table:: true
  query-properties:: [:block]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-26 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-08-26 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-27 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-08-27 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :remark]
  query-sort-by:: block
  query-sort-desc:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-28 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-08-28 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-29 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-08-29 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-30 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2024-08-30 Fri")
  ]}
  #+END_QUERY