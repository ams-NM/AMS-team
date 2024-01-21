- {{renderer :smartblock, weekly-tp, create weekly view (To remove "[[]]"), true}}
- filters:: {"weekly" false}
- [Last Week]([[Weekly/]]) << | >> [Next Week]([[Weekly/]])
- #+BEGIN_QUERY
  {:title [:h2 "[[2024-01-01 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-01-01 Mon")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2024-01-02 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-01-02 Tue")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2024-01-03 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-01-03 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2024-01-04 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-01-04 Thu")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2024-01-05 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-01-05 Fri")
  ]}
  #+END_QUERY
-