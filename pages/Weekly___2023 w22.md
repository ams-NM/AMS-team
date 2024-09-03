-
- [Last Week]([[Weekly/2023 w21]]) << | >> [Next Week]([[Weekly/2023 w23]])
- query-table:: true
  query-properties:: [:block :finish :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-29 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-29 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-30 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-30 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-31 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-31 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-01 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-06-01 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-02 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-06-02 Fri")
  ]}
  #+END_QUERY
-