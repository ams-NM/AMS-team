filters:: {"🏠nm tasks & schedule" false}

- [[VCS Console Relocation Proof Of Concept]]
- [[SMG Extend Forecaster Control in PTB NE 3F]]
- #+BEGIN_QUERY
  {:title [:H2 "Ongoing"]
   :query [:find ?name
         :in $ ?tag
         :where
         (page-property ?p :status "ongoing")
         [?t :block/name ?tag]
         [?p :page/tags ?t]
         [?p :block/name ?name]]
   :inputs ["cwo"]
   :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "#/page/" page)} (clojure.string/capitalize page)])])}
  #+END_QUERY
-
- #+BEGIN_QUERY
  {:title [:H2 "Done"]
   :query [:find ?name
         :in $ ?tag
         :where
         (page-property ?p :status "done")
         [?t :block/name ?tag]
         [?p :page/tags ?t]
         [?p :block/name ?name]]
   :inputs ["cwo"]
   :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "#/page/" page)} (clojure.string/capitalize page)])])}
  #+END_QUERY
-