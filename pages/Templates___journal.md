- ```clojure
  #+BEGIN_QUERY
   {:title [:h2 "⚠️ OVERDUE"]
    :query [:find (pull ?b [*])
            :in $ ?today
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            [?b :block/properties ?prop]
            [(get ?prop :plan) ?plan]
            [(< ?plan ?today)]
            ]
    :inputs [:today]}
    :collapsed? false}
  #+END_QUERY
  
  
  ```
- #+BEGIN_QUERY
   {:title [:h2 "⚠️ OVERDUE"]
    :query [:find (pull ?b [*])
            :in $ ?start ?today
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            [(< (property ?b :plan) ?today)]
            ]
    :inputs [:-56d :today]
    :collapsed? false}
  #+END_QUERY
-