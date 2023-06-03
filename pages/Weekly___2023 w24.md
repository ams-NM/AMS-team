filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w23]]) << | >> [Next Week]([[Weekly/2023 w25]])
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-12 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-12 Mon")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-13 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-13 Tue")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-14 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-14 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-15 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-15 Thu")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-06-16 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-06-16 Fri")
  ]}
  #+END_QUERY
-