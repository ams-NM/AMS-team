query-table:: true
query-properties:: [:plan :block]
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

- #+BEGIN_QUERY
  {:title [:h2 "Tuesday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-11 Tue")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "Wednesday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-12")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "Thursday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-10 Mon")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h2 "Friday"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO" "DONE"})
           (property ?b :plan "2023-04-10 Mon")
  ]}
  #+END_QUERY