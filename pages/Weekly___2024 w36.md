filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w35]]) << | >> [Next Week]([[Weekly/2024 w37]])
- query-table:: true
  query-properties:: [:block :plan :finished :remark :page]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-09-02 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-09-02 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-09-03 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-09-03 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-09-04 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-09-04 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-09-05 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-09-05 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :finished :remark :page]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-09-06 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-09-06 Fri")
  ]}
  #+END_QUERY
-
-