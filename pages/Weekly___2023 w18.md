- [Last Week]([[Weekly/2023 w17]]) << | >> [Next Week]([[Weekly/2023 w19]])
- query-table:: true
  query-properties:: [:block :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-01 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-01 Mon")
  ]}
  #+END_QUERY
- query-properties:: [:block :finished :remark]
  query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-02 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-02 Tue")
  ]}
  #+END_QUERY
- query-properties:: [:block :finished :remark]
  query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-03 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-03 Wed")
  ]}
  #+END_QUERY
- query-properties:: [:block]
  query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-04 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-04 Thu")
  ]}
  #+END_QUERY
- query-properties:: [:block]
  query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-05-05 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-05-05 Fri")
  ]}
  #+END_QUERY
-