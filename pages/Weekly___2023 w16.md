- Test
  template:: test-wk-tp
	- #+BEGIN_QUERY
	  {:title [:h2 "<%setinput: monday%>"]
	   :query [:find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           (property ?b :plan "<%getinput: monday%>")
	  ]}
	  #+END_QUERY
-
-
- {{renderer :smartblock, test-wk-tp, create weekly view, true}}
-
-
-
-
-
- template:: www-tp
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
-
-
-
- template:: wwww-tp
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
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-