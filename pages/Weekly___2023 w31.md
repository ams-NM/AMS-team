filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w30]]) << | >> [Next Week]([[Weekly/]])
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-31 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-31 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-08-01 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-08-01 Tue")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-08-02 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-08-02 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-08-03 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-08-03 Thu")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-08-04 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-08-04 Fri")
  ]}
  #+END_QUERY