filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w28]]) << | >> [Next Week]([[Weekly/2023 w30]])
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-17 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-17 Mon")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-18 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-18 Tue")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-19 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-19 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-20 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-20 Thu")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-07-21 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-21 Fri")
  ]}
  #+END_QUERY