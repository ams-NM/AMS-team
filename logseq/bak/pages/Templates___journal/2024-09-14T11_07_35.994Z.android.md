type:: templates

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
  
  #+BEGIN_QUERY
   {:title [:h2 "Today"]
    :query [:find (pull ?b [*])
            :in $ ?current-page
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            [?p :block/name ?current-page]
            [?p :block/journal? true]
            [?p :block/journal-day ?today]
            [?b :block/properties ?prop]
            [(get ?prop :plan) ?plan]
            [(= ?plan ?today)]
            ]
    :inputs [:current-page]}
    :collapsed? false}
  #+END_QUERY
  
  #+BEGIN_QUERY
   {:title [:h2 "Today"]
    :query [:find (pull ?b [*])
            :in $ ?today
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            [?b :block/properties ?prop]
            [(get ?prop :plan) ?pd]
            [(?pd ?today)]
            ]
    :inputs [:current-page]
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