filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w19]]) << | >> [Next Week]([[Weekly/2023 w21]])
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-15 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-15 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-16 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-16 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-17 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-17 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[ 2023-05-18 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-18 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  query-sort-by:: finished
  query-sort-desc:: false
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-19 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-19 Fri")
  ]}
  #+END_QUERY