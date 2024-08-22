filters:: {"weekly" false}

- [Last Week]([[Weekly/2023 w29]]) << | >> [Next Week]([[Weekly/2023 w31]])
- Test query using `Live query`
  collapsed:: true
	- {{query (and (task TODO DONE) (property :plan [[2023-07-24 Mon]]))}}
	  query-table:: true
	  query-properties:: [:block :finished :remark]
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-24 Mon]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-24 Mon")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-25 Tue]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-25 Tue")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-26 Wed]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-26 Wed")
  ]}
  #+END_QUERY
- #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-27 Thu]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-27 Thu")
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :finished :remark]
  #+BEGIN_QUERY
  {:title [:h3 "[[2023-07-28 Fri]]"]
  :query [:find (pull ?b [*])
       :where
       [?b :block/parent ?parent]
       (not (has-property ?parent :template))
       (task ?b #{"TODO" "DONE"})
       (property ?b :plan "2023-07-28 Fri")
  ]}
  #+END_QUERY