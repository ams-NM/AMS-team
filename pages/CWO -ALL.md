filters:: {"🏠nm tasks & schedule" false}

- [[VCS Console Relocation Proof Of Concept]]
- [[SMG Extend Forecaster Control in PTB NE 3/F]]
- #+BEGIN_QUERY
  {:title [:H2 "🏋️CWO Ongoing"]
   :query [:find ?name
         :in $ ?tag
         :where
         (page-property ? :status "ongoing")
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
  {:title [:H2 "🏋️CWO Done"]
   :query [:find ?name
         :in $ ?tag
         :where
         (page-property ? :status "done")
         [?t :block/name ?tag]
         [?p :page/tags ?t]
         [?p :block/name ?name]]
   :inputs ["cwo"]
   :view (fn [result]
         [:div.flex.flex-col
          (for [page result]
            [:a {:href (str "#/page/" page)} (clojure.string/capitalize page)])])}
  #+END_QUERY
- ## Done
	- ### SMG Extend Forecaster Control in PTB NE 3/F
	  start:: [[2023-01-19 Thu]] 
	  status:: done
	  complete:: [[2023-04-03 Mon]] 
	  estimated-hours::
	  tags:: cwo, [[SMG Extend Forecaster Control in PTB NE 3/F]] 
	  wo:: CWO23011