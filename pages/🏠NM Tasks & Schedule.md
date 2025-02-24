- Press ==tw== keys to toggle page width.
- ==Data auto updates== at the 15th minute every hour.
- ### 🌜️Current Month: [[Monthly/2025-02]]
- ### 7️⃣ Current week: [[Weekly/2025 w09]]
- query-table:: true
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "😵‍💫BACKLOG"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "aaron"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:-1y :-1d]
   }
  #+END_QUERY
- query-sort-by:: block
  query-table:: true
  query-sort-desc:: true
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "⏰TODAY"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "aaron"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:today :today]
   }
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :date]
  #+BEGIN_QUERY
  {
   :title [:h2 "🗓️Schedule of Tomorrow"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "aaron"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:+1d :+1d]
   }
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :date]
  collapsed:: true
  #+BEGIN_QUERY
  {
   :title [:h2 "📌Outstanding"]
   :query [
           :find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO"})
           [?p :block/name "outstanding"]
           [?b :block/refs ?p]
           ]
   }
  #+END_QUERY
- query-sort-by:: date
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:date :block]
  collapsed:: true
  #+BEGIN_QUERY
  {
   :title [:h2 "🗓️Schedule of Next 30 days"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?end
           :where
           [?b :block/properties ?properties]
           [(get ?properties :date) ?bn]
           (task ?b #{"TODO"})
           [?b :block/refs ?p]
           (not [?b :block/path-refs [:block/name "aaron"]])
           [?p :page/journal? true]
           [?p :page/journal-day ?dnum]
           [?p :page/original-name ?jn]
           [(<= ?start ?dnum ?end)]
           [(contains? ?bn ?jn)]
           ]
  :inputs [:+1d :+30d]
   }
  #+END_QUERY
- ## ⏰Tasks for [[Aaron]] <mark class='green'>ONLY</mark>
  collapsed:: true
	- query-table:: true
	  query-properties:: [:block :date]
	  #+BEGIN_QUERY
	  {
	   :title [:h4 "🎯 TODO"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           (task ?b #{"TODO"})
	           [?pt :block/name "aaron"]
	           [?b :block/refs ?pt]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:-1m :today]
	   }
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block]
	  #+BEGIN_QUERY
	  {
	   :title [:h4 "✅ DONE"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           (task ?b #{"DONE"})
	           [?b :block/refs ?p]
	           [?b :block/path-refs [:block/name "aaron"]]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:today :today]
	   }
	  #+END_QUERY
	- query-sort-by:: date
	  query-table:: true
	  query-sort-desc:: false
	  query-properties:: [:block :date]
	  collapsed:: true
	  #+BEGIN_QUERY
	  {
	   :title [:h2 "🗓️Aaron's Errands for Next 30 days"]
	   :query [
	           :find (pull ?b [*])
	           :in $ ?start ?end
	           :where
	           [?b :block/properties ?properties]
	           [(get ?properties :date) ?bn]
	           (task ?b #{"TODO"})
	           [?b :block/refs ?p]
	           [?b :block/path-refs [:block/name "aaron"]]
	           [?p :page/journal? true]
	           [?p :page/journal-day ?dnum]
	           [?p :page/original-name ?jn]
	           [(>= ?dnum ?start)]
	           [(<= ?dnum ?end)]
	           [(contains? ?bn ?jn)]
	           ]
	  :inputs [:today :+30d]
	   }
	  #+END_QUERY
- query-table:: true
  query-properties:: [:block :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {
   :title [:h2 "⏳Pending"]
   :query [
           :find (pull ?b [*])
           :where
           [?b :block/parent ?parent]
           (not (has-property ?parent :template))
           (task ?b #{"TODO"})
           [?p :block/name "pending"]
           [?b :block/refs ?p]
           ]
   }
  #+END_QUERY
- ## 🏋️CWO Ongoing
  collapsed:: true
	- query-properties:: [:block]
	  #+BEGIN_QUERY
	  {:title [:H2 "CWO"]
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
- ## ⏳[[Calibration]] - [[AWOS]]
  id:: 674ff35a-5e43-42be-839f-7094fb7be50d
  collapsed:: true
	- ### HMP
		- {{query (and [[Calibration/HMP]] #cal-due )}}
		  query-table:: true
		  query-properties:: [:block :due :out :sn :location :remark]
		  query-sort-by:: due
		  query-sort-desc:: false
	- ### PTB
		- {{query (and [[Calibration/PTB]] #cal-due )}}
		  query-table:: true
		  query-properties:: [:block :due :out :sn :location :remark]
		  query-sort-by:: due
		  query-sort-desc:: false
- query-table:: true
  query-properties:: [:block :pr :wo :issued]
  collapsed:: true
  #+BEGIN_QUERY
  {
  :title [:H2 "🛒PR Pending"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "pr-pending"]
           (not [?b :block/path-refs [:block/name "templates/misc"]])
           [?b :block/refs ?p]
  ]}
  #+END_QUERY
- query-table:: true
  query-properties:: [:block :wo :issued :remark]
  collapsed:: true
  #+BEGIN_QUERY
  {
  :title [:H2 "🛒IMO Pending"]
  :query [:find (pull ?b [*])
           :where
           (task ?b #{"TODO"})
           [?p :block/name "imo-pending"]
           (not [?b :block/path-refs [:block/name "templates/misc"]])
           [?b :block/refs ?p]
  ]}
  #+END_QUERY