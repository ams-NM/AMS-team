-
- query-table:: true
  query-properties:: [:block :plan :finished]
  #+BEGIN_QUERY
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
  query-properties:: [:block :plan]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-18 Tue]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-18 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-19 Wed]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-19 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :remark]
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-20 Thu]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-20 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-21 Fri]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-21 Fri")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-22 Sat]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-22 Sat")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-23 Sun]]"]
   :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-04-23 Sun")
  ]}
  #+END_QUERY