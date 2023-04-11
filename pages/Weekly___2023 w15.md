query-table:: true
query-properties:: [:plan :block :finished]
query-sort-by:: block
query-sort-desc:: false
#+BEGIN_QUERY
{:title [:h2 "Monday"]
 :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         (property ?b :plan "2023-04-10 Mon")
]}
#+END_QUERY

- query-table:: true
  query-properties:: [:plan :block :finished]
  #+BEGIN_QUERY
  {:title [:h2 "Tuesday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-11 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block :remark]
  #+BEGIN_QUERY
  {:title [:h2 "Wednesday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-12 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block]
  #+BEGIN_QUERY
  {:title [:h2 "Thursday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-13 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:plan :block]
  #+BEGIN_QUERY
  {:title [:h2 "Friday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-14 Fri")
  ]}
  #+END_QUERY