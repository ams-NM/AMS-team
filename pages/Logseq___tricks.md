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
	- ### Excluding a page
		- ```
		  #+BEGIN_QUERY
		  {:title "**Current Missions**"
		   :query [:find (pull ?b [*])
		       :where
		       [?b :block/marker ?marker]
		       [(contains? #{"TODO"} ?marker)]
		       (not [?b :block/path-refs [:block/name "templates/misc"]])
		       ]
		       }
		  #+END_QUERY
		  ```
		- ### Comparing dates of value of block property with ==today==
			- ```
			  #+BEGIN_QUERY
			  {
			   :title [:h2 "🗓️Schedule for Next 7 days"]
			   :query [
			           :find (pull ?b [*])
			           :in $ ?start ?end
			           :where
			           [?b :block/properties ?properties]
			           [(get ?properties :date) ?bn]
			           (task ?b #{"TODO"})
			           [?b :block/refs ?p]
			           [?p :page/journal? true]
			           [?p :page/journal-day ?dnum]
			           [?p :page/original-name ?jn]
			           [(>= ?dnum ?start)]
			           [(<= ?dnum ?end)]
			           [(contains? ?bn ?jn)]
			           ]
			  :inputs [:+1d :+7d]
			   }
			  #+END_QUERY
			  ```
- Git Commit Hooks
	- Put the following 2 files in ==.git/hooks/==
		- ==pre-commit==
		  collapsed:: true
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
		  collapsed:: true
			- ```bash
			  #!/bin/sh
			  
			  git push origin main
			  ```
- [[How to publish Logseq graph to GitHub Pages]]
- Page Icon
  collapsed:: true
	- `icon::` supports emojis and Unicode glyphs ([nerd fonts](https://www.nerdfonts.com/))
	- Ref: https://discuss.logseq.com/t/using-font-awesome-icons/3666
		- 1. Install a Nerd Font 
		  2. add the following to `/logseq/custom.css`, remember to modify ==font-family== accordingly.
			- ```css
			  :root {
			    --ct-text-size: 14px;
			    --ct-line-height: 1.6;
			    --ls-font-family: "FontAwesome", sans-serif;
			    --ct-page-title-font-family: var(--ls-font-family);
			    --ct-code-font-family: "Ubuntu Nerd Font";
			  }
			  ```
-