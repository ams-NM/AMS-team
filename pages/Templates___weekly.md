type:: templates

- Weekly Smartblock Button
  template:: weekly-smartblock-tp
  template-including-parent:: false
	- {{renderer :smartblock, weekly-tp, create weekly view (Use short-cut key ";;nbdn" to get week dates without "[[]]". Remove this Block), true}}
	-
- Weekly Tasks
  query-table:: true
  query-properties:: [:plan :block]
  template:: weekly-tp
  template-including-parent:: false
	- filters:: {"weekly" false}
	- TODO Add page links to ==Last Week== and ==Next Week==
	- [Last Week]([[Weekly/]]) << | >> [Next Week]([[Weekly/]])
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:h2 "[[<%setinput: Monday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :plan "<%getinput: Monday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:h2 "[[<%setinput: Tuesday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :plan "<%getinput: Tuesday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:h2 "[[<%setinput: Wednesday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :plan "<%getinput: Wednesday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:h2 "[[<%setinput: Thursday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :plan "<%getinput: Thursday%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:h2 "[[<%setinput: Friday%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :plan "<%getinput: Friday%>")
	  ]}
	  #+END_QUERY
	-