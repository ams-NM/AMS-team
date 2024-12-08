type:: templates

- Weekly Smartblock Button
  template:: weekly-smartblock-tp
  template-including-parent:: false
	- {{renderer :smartblock, weekly-tp, create weekly view (Use short-cut key ";;nbdn" to get week dates without "[[]]". Remove this Block), true}}
	-
- Weekly Tasks
  query-table:: true
  query-properties:: [:date :block]
  template:: weekly-tp
  template-including-parent:: false
	- filters:: {"weekly" false}
	- [Last Week]([[Weekly/]]) << | >> [Next Week]([[Weekly/]])
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Monday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Monday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Tuesday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Tuesday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Wednesday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Wednesday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Thursday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Thursday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Friday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Friday%>")
	  ]}
	  #+END_QUERY
	-