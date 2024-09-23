type:: templates

- Calibration
  template:: cal-due
  template-including-parent:: false
  collapsed:: true
	- [[sensor??]] 
	  tags:: cal-due
	  due::
	  out::
	  sn::
	  wo:: 
	  remark::
- Holidays
  template:: holidays-tp
  template-including-parent:: false
  collapsed:: true
	- ## 202X
		- TODO [[New Year's Day]] [[PH]]
		  date::
		- TODO [[Chinese New Year]] `Day 1` [[PH]] 
		  date::
		- TODO [[Chinese New Year]] `Day 2` [[PH]] 
		  date::
		- TODO [[Chinese New Year]] `Day 3` [[PH]] 
		  date::
		- TODO `Compensation` for [[Chinese New Year]] `Day 1` [[CH]]
		  date::
		- TODO [[Good Friday]] [[CH]]
		  date::
		- TODO [[Easter Monday]] [[CH]]
		  date::
		- TODO [[Cheng Ming Festival]] [[PH]]
		  date::
		- TODO [[Labor Day]] [[PH]]
		  date::
		- TODO [[Birthday of Buddha]] [[CH]]
		  date::
		- TODO [[Dragon Boat Festival]] [[CH]]
		  date::
		- TODO [[Mid-Autumn Festival]] [[PH]]
		  date::
		- TODO [[National Day]] `Day 1` [[PH]]
		  date::
		- TODO [[National Day]] `Day 2` [[PH]]
		  date::
		- TODO `Compensation` for [[National Day]] `Day 1` [[CH]] 
		  date::
		- TODO [[Festival of Ancestors]] [[PH]]
		  date::
		- TODO [[Macau Establishment Day]] [[PH]]
		  date::
		- TODO [[Winter Solstice]] [[CH]]
		  date::
		- TODO [[Christmas Eve]] [[CH]]
		  date::
		- TODO [[Christmas Day]] [[CH]]
		  date::
- Task
  template:: todo-tp
  template-including-parent:: false
  collapsed:: true
	- TODO 
	  done:: #{"{"}
	  date::
- CWO
  template:: cwo-tp
  template-including-parent:: false
  collapsed:: true
	- start:: 
	  status:: ongoing
	  complete:: 
	  estimated-hours:: 
	  tags:: cwo
	  wo:: CWOxxxx
	  remark::
	- ## Ref:
	- ## TODOs
	- ## Logs
	-
- PR
  template:: pr-tp
  template-including-parent:: false
  collapsed:: true
	- TODO item-name???
	  tags:: PR, PR-pending
	  pr:: 
	  wo:: 
	  issued:: 
	  received::
- IMO
  template:: imo-tp
  template-including-parent:: false
  collapsed:: true
	- TODO item-name???
	  tags:: IMO, IMO-pending
	  wo:: 
	  issued:: 
	  received::
- Event
  template:: event-tp
  template-including-parent:: false
  collapsed:: true
	- [[event???]]
	  tags:: event
	  start:: 
	  end:: 
	  status::
- Person -Icon was not showed in link
  template:: person-tp
  template-including-parent:: false
  collapsed:: true
	- icon:: 👤
	  type:: person
	  categories:: colleague, nm-team
- [[Typhoon Standby]] [[person?]] [[typhoon-name?]]
  template:: typhoon-standby-tp
  date:: 
  end:: 
  duration::
- [[Maximo]] Labor Data
  template:: labor-smartblock-tp
  template-including-parent:: false
	- {{renderer :smartblock, labor-query-tp, Click to create labor view (Remove this Block AFTER use), true}}
	- Labor Data 
	  template:: labor-query-tp
	  collapsed:: true
		- #+BEGIN_QUERY
		  {
		   :title [:h3 "Labor Data - [[Aaron]] "]
		   :query [
		           :find (pull ?b [*])
		           :in $ ?start ?end [?staff ...]
		           :where
		           [?b :block/parent ?parent]
		           (not (has-property ?parent :template))
		           (task ?b #{"TODO" "DONE"})
		           [?b :block/path-refs [:block/name "labor-todo"]]
		           [?b :block/refs ?p]
		           [?p :page/journal? true]
		           [?p :page/journal-day ?dnum]
		           [?p :page/original-name ?jn]
		           [(<= ?start ?dnum ?end)]
		           [?b :block/properties ?properties]
		           [(get ?properties :date) ?bn]
		           [(contains? ?bn ?jn)]
		           [(get ?properties :staffs) ?stfs]
		           [(contains? ?stfs ?staff)]
		           ]
		  :inputs [<%setinput: StartDate(e.g. 20240901)%> <%setinput: EndDate(e.g. 20240930)%> ["Aaron" "All-staffs"]]
		   }
		  #+END_QUERY
		- #+BEGIN_QUERY
		  {
		   :title [:h3 "Labor Data - [[Eric]] "]
		   :query [
		           :find (pull ?b [*])
		           :in $ ?start ?end [?staff ...]
		           :where
		           [?b :block/parent ?parent]
		           (not (has-property ?parent :template))
		           (task ?b #{"TODO" "DONE"})
		           [?b :block/path-refs [:block/name "labor-todo"]]
		           [?b :block/refs ?p]
		           [?p :page/journal? true]
		           [?p :page/journal-day ?dnum]
		           [?p :page/original-name ?jn]
		           [(<= ?start ?dnum ?end)]
		           [?b :block/properties ?properties]
		           [(get ?properties :date) ?bn]
		           [(contains? ?bn ?jn)]
		           [(get ?properties :staffs) ?stfs]
		           [(contains? ?stfs ?staff)]
		           ]
		  :inputs [<%getInput: StartDate(e.g. 20240901)%> <%getInput: EndDate(e.g. 20240930)%> ["Eric" "All-staffs"]]
		   }
		  #+END_QUERY
		- #+BEGIN_QUERY
		  {
		   :title [:h3 "Labor Data - [[Nick]] "]
		   :query [
		           :find (pull ?b [*])
		           :in $ ?start ?end [?staff ...]
		           :where
		           [?b :block/parent ?parent]
		           (not (has-property ?parent :template))
		           (task ?b #{"TODO" "DONE"})
		           [?b :block/path-refs [:block/name "labor-todo"]]
		           [?b :block/refs ?p]
		           [?p :page/journal? true]
		           [?p :page/journal-day ?dnum]
		           [?p :page/original-name ?jn]
		           [(<= ?start ?dnum ?end)]
		           [?b :block/properties ?properties]
		           [(get ?properties :date) ?bn]
		           [(contains? ?bn ?jn)]
		           [(get ?properties :staffs) ?stfs]
		           [(contains? ?stfs ?staff)]
		           ]
		  :inputs [<%getinput: StartDate(e.g. 20240901)%> <%getinput: EndDate(e.g. 20240930)%> ["Nick" "All-staffs"]]
		   }
		  #+END_QUERY
		- #+BEGIN_QUERY
		  {
		   :title [:h3 "Labor Data - [[Vincent]] "]
		   :query [
		           :find (pull ?b [*])
		           :in $ ?start ?end [?staff ...]
		           :where
		           [?b :block/parent ?parent]
		           (not (has-property ?parent :template))
		           (task ?b #{"TODO" "DONE"})
		           [?b :block/path-refs [:block/name "labor-todo"]]
		           [?b :block/refs ?p]
		           [?p :page/journal? true]
		           [?p :page/journal-day ?dnum]
		           [?p :page/original-name ?jn]
		           [(<= ?start ?dnum ?end)]
		           [?b :block/properties ?properties]
		           [(get ?properties :date) ?bn]
		           [(contains? ?bn ?jn)]
		           [(get ?properties :staffs) ?stfs]
		           [(contains? ?stfs ?staff)]
		           ]
		  :inputs [<%getinput: StartDate(e.g. 20240901)%> <%getinput: EndDate(e.g. 20240930)%> ["Vincent" "All-staffs"]]
		   }
		  #+END_QUERY