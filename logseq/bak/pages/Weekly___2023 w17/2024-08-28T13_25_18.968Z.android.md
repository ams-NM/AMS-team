- [Last Week]([[Weekly/2023 w16]]) << | >> [Next Week]([[Weekly/2023 w18]])
- query-table:: true
  query-properties:: [:block :finished]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-24 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-24 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-25 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-25 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-26 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-26 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-27 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-27 Thu")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-28 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-28 Fri")
  ]}
  #+END_QUERY
-