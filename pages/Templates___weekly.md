type:: templates

- Weekly Smartblock Button
  template:: weekly-smartblock-tp
  template-including-parent:: false
	- {{renderer :smartblock, weekly-tp, create weekly view (Use short-cut key ";;nbmon" to get week dates without "[[]]". Remove this Block), true}}
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
	  {:title [:h3 "[[<%setinput: Monday(;;nb>mon)%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Monday(;;nb>mon)%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Tuesday(;;nb>tue)%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Tuesday(;;nb>tue)%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Wednesday(;;nb>wed)%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Wednesday(;;nb>wed)%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Thursday(;;nb>thu)%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Thursday(;;nb>thu)%>")
	  ]}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:h3 "[[<%setinput: Friday(;;nb>fri)%>]]"]
	   :query [:find (pull ?b [*])
	         :where
	         [?b :block/parent ?parent]
	         (not (has-property ?parent :template))
	         (task ?b #{"TODO" "DONE"})
	         (property ?b :date "<%getinput: Friday(;;nb>fri)%>")
	  ]}
	  #+END_QUERY