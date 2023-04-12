- Test
  template:: test-wk-tp
	- #+BEGIN_QUERY
	  {:title [:h2 "<%setinput: monday%>"]
	   :query [:find (pull ?b [*])
	           :where
	           [?b :block/parent ?parent]
	           (not (has-property ?parent :template))
	           (task ?b #{"TODO" "DONE"})
	           [?b :block/properties ?props]
	           [(get ?props :plan) ?plan]
	           [(contains? "<%getinput: monday%>" ?plan)]
	  ]}
	  #+END_QUERY
-
-
- {{renderer :smartblock, test-wk-tp, create weekly view, true}}
- #+BEGIN_QUERY
  {:title [:h2 "[[2023-04-10 Mon]]"]
   :query [:find (pull ?b [*])
         :where
         [?b :block/parent ?parent]
         (not (has-property ?parent :template))
         (task ?b #{"TODO" "DONE"})
         [?b :block/properties ?props]
         [(get ?props :plan) ?plan]
         [(= "[[2023-04-10 Mon]]" ?plan)]
  ]}
  #+END_QUERY
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