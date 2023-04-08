- ```clojure
  #+BEGIN_QUERY
   {:title "⚠️ OVERDUE"
    :query [:find (pull ?b [*])
            :in $ ?start ?today
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            (< property ?b :plan ?today)]
    :inputs [:-30d :today]
    :collapsed? false}
  #+END_QUERY
  ```
- #+BEGIN_QUERY
   {:title [:h2 "⚠️ OVERDUE"]
    :query [:find (pull ?b [*])
            :in $ ?start ?today
            :where
            (task ?b #{"NOW" "LATER" "TODO" "DOING"})
            (< property ?b :plan ?today)]
    :inputs [:-56d :today]
    :collapsed? false}
  #+END_QUERY
-