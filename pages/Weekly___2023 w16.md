-
- {{renderer :smartblock, weekly-tp, weekly, true}}
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-17 Mon]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-17 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block]
  #+BEGIN_QUERY
  {:title [:h2 "[[Tue]]"]
   :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         (property ?b :plan "Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[Wed]]"]
   :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         (property ?b :plan "Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block]
  #+BEGIN_QUERY
  {:title [:h2 "[[Thu]]"]
   :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         (property ?b :plan " Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block]
  #+BEGIN_QUERY
  {:title [:h2 "[[Fri]]"]
   :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         (property ?b :plan " Fri")
  ]}
  #+END_QUERY
-
-
-
-
-
-
-