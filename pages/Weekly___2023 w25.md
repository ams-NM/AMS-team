filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w24]]) << | >> [Next Week]([[Weekly/2023 w26]])
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-19 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-19 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-20 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-20 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-21 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-21 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-22 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-22 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-23 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-23 Fri")
  ]}
  #+END_QUERY
-