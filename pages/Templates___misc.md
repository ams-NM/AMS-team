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
	- ## 202X
	- TODO [[New Year's Day]] [[PH]]
	  date::
	- TODO [[Chinese New Year]] `Day 1`
	  date::
	- TODO [[Chinese New Year]] `Day 2`
	  date::
	- TODO [[Chinese New Year]] `Day 3`
	  date::
	-
- Task
  template:: todo-tp
  template-including-parent:: false
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
-