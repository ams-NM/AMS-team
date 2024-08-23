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
- Task
  template:: todo-tp
  template-including-parent:: false
  collapsed:: true
	- TODO 
	  done:: #{"{"}
	  plan:: 
	  finished::
	  remark::
- CWO
  template:: cwo-tp
  template-including-parent:: false
  collapsed:: true
	- ### <Description>
	  start::
	  status:: ongoing
	  complete::
	  estimated-hours::
	  tags:: cwo
	  wo:: CWOxxxx
- PR
  template:: pr-tp
  template-including-parent:: false
	- TODO item-name???
	  tags:: PR, PR-pending
	  pr:: 
	  wo:: 
	  issued:: 
	  received::
- IMO
  template:: imo-tp
  template-including-parent:: false
	- TODO item-name???
	  tags:: IMO, IMO-pending
	  wo::
	  issued::
	  received::
- Event
  template:: event-tp
  template-including-parent:: false
	- [[event???]]
	  tags:: event
	  start:: 
	  end:: 
	  status::
- Person -Icon was not showed in link
  template:: person-tp
  template-including-parent:: false
	- icon:: 👤
	  type:: person
	  categories:: colleague, nm-team