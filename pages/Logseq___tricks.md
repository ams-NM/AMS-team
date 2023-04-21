- Query on Journals - in ==config.edn==
  collapsed:: true
	- It adds queries of tasks on `journal` pages:
	- ```edn
	  :default-queries
	   {:journals
	    [{:title               "🔨 NOW"
	      :query            [:find (pull ?p [*])
	                         :in $ ?start ?today
	                         :where
	                         [?p :block/marker ?marker]
	                         [(contains? #{"NOW" "DOING"} ?marker)]]
	      :inputs           [:365d :today]
	      :result-transform (fn [result]
	                               (sort-by (fn [h]
	                                     (get h :block/priority "Z")) result))
	      :collapsed?       false
	      :breadcrumb-show? false}  
	  
	  {:title "❓ Random Block"
	   :query [:find (pull ?b [*])
	           :where
	           [?b :block/content ?content]
	           (not [(empty? ?content)])]
	   :result-transform (fn [result]
	                       [(rand-nth result)])
	   :collapsed? false}
	     {:title         "🔥 OVERDUE"
	      :query         [:find (pull ?b [*])
	                  :in $ ?start ?next
	                  :where
	                  [?b :block/marker ?marker]
	                  (or [?b :block/scheduled ?d]
	                  [?b :block/deadline ?d])
	                  [(contains? #{"TODO" "DOING" "NOW" "LATER" "WAITING"} ?marker)]
	                  [(>= ?d ?start)]
	                  [(<= ?d ?next)]]
	      :inputs [:365d :1d]
	      :result-transform (fn [result]
	                               (sort-by (fn [h]
	                                     (get h :block/priority "Z")) result))
	      :collapsed? false
	      :breadcrumb-show? false}
	  
	  {:title "📚Backlog"
	  :query [:find (pull ?todo [*]) :in $ ?current-page
	  :where
	  [?p :block/name ?current-page]
	  [?todo :block/marker ?marker]
	  (not [?todo :block/page ?p])
	  (not [_ :block/refs ?todo])
	  [(contains? #{"TODO" "DOING"} ?marker)]
	  (or-join [?todo]
	         (and  [?todo :block/page ?page]
	                  [?page :block/properties ?props]
	                  [(get ?props :is) ?is]
	                  [(= ?is "active")] )
	         (and [?todo :block/page ?page]
	                 (not-join [?todo]
	                               [?todo :block/refs ?ref]
	                               [?ref :block/journal? true])
	                 [(missing? $ ?page :block/properties)])
	  ) ]
	  :inputs [:current-page]}
	     {:title      "📅 NEXT"
	      :query      [:find (pull ?p [*])
	                   :in $ ?start ?next
	                   :where
	                   [?p :block/marker ?marker]
	                   (or [?p :block/scheduled ?d]
	                    [?p :block/deadline ?d]
	                   [?p :block/journal-day ?d])
	                   [(contains? #{"NOW" "LATER" "TODO" "WAITING"} ?marker)]
	                   [(> ?d ?start)]
	                   [(< ?d ?next)]]
	      :inputs     [:today :7d-after]
	      :result-transform (fn [result]
	                               (sort-by (fn [h]
	                                     (get h :block/priority "Z")) result))
	      :collapsed? false
	      :breadcrumb-show? false}
	  ]}
	  ```
- Advanced query
  collapsed:: true
	- https://bgrolleman.gitlab.io/logseq_publish_toolsontech/#/page/logseq%2Fadvanced%20queries
	- https://charleschiugit.github.io/page/logseq/queries/
	-
- Git Commit Hooks
  collapsed:: true
	- Put the following 2 files in ==.git/hooks/==
		- ==pre-commit==
			- ```bash
			  #!/bin/sh
			  #
			  #
			  # Pull before committing
			  # Credential handling options:
			  #  - hardcode credentials in URL
			  #  - use ssh with key auth
			  #  - https://git-scm.com/docs/git-credential-store
			  #  - git credential helper on windows
			  
			  # Redirect output to stderr, uncomment for more output for debugging
			  # exec 1>&2
			  
			  output=$(git pull --no-rebase)
			  
			  # Handle non error output as otherwise it gets shown with any exit code by logseq
			  if [ "$output" = "Already up to date." ]; then
			      # no output
			      :
			  else
			      # probably error print it to screen
			      echo "${output}"
			  fi
			  
			  git add -A
			  ```
		- ==post-commit==
			- ```bash
			  #!/bin/sh
			  
			  git push origin main
			  ```
- [[How to publish Logseq graph to GitHub Pages]]