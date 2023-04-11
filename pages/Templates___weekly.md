- Weekly Tasks
  query-table:: true
  query-properties:: [:plan :block]
  type:: templates
  template:: weekly-tp
  template-including-parent:: false
	- #+BEGIN_QUERY
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