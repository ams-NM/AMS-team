## [[Calibration]]
collapsed:: true
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:H3 "HMP"]
	   :query [:find (pull ?b [*])
	       :where
	       [?p :block/name "cal-due"]
	       [?b :block/path-refs [:block/name "calibration/hmp"]]
	       (not [?b :block/path-refs [:block/name "templates/misc"]])
	       (not [?b :block/path-refs [:block/name "workflows"]])
	       ]}
	  #+END_QUERY
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title [:H3 "PTB"]
	   :query [:find (pull ?b [*])
	       :where
	       [?p :block/name "cal-due"]
	       [?b :block/path-refs [:block/name "calibration/ptb"]]
	       (not [?b :block/path-refs [:block/name "templates/misc"]])
	       (not [?b :block/path-refs [:block/name "workflows"]])
	       ]}
	  #+END_QUERY
- Task todo with tag `outstanding`
	- #+BEGIN_QUERY
	  {
	  :title [:H2 "📌Outstanding"]
	  :query [:find (pull ?b [*])
	           :where
	           (task ?b #{"TODO"})
	           [?p :block/name "outstanding"]
	           [?b :block/refs ?p]]}
	  #+END_QUERY