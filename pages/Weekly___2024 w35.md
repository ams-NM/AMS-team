filters:: {"weekly" false}

- [Last Week]([[Weekly/2024 w34]]) << | >> [Next Week]([[Weekly/2024 w36]])
- Test Live query
	- {{query and ( (task todo done) (property :plan "2024-08-26 Mon") ) }}
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-26 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-08-26 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-27 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-08-27 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-28 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-08-28 Wed")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-29 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-08-29 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :plan :finish :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2024-08-30 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2024-08-30 Fri")
  ]}
  #+END_QUERY
-
-
-