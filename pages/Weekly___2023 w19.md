- [Last Week]([[Weekly/2023 w18]]) << | >> [Next Week]([[Weekly/2023 w20]])
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-08 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-08 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-09 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-09 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-10 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-10 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-11 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-11 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-12 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-12 Fri")
  ]}
  #+END_QUERY
-