filters:: {"weekly" false}

-
- [Last Week]([[Weekly/2023 w20]]) << | >> [Next Week]([[Weekly/2023 w22]])
- query-table:: true
  query-properties:: [:block :finish :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-22 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-22 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-23 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-23 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-24 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-24 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-25 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-25 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finish :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-26 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :date "2023-05-26 Fri")
  ]}
  #+END_QUERY