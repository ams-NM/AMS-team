filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w22]]) << | >> [Next Week]([[Weekly/2023 w24]])
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-05 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-05 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-06 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-06 Tue")
  ]}
  #+END_QUERY
- query-table:: false
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-07 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-07 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-08 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-08 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-09 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-09 Fri")
  ]}
  #+END_QUERY
-