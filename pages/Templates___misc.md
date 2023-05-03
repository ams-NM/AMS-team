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
	-
- PR
  template:: pr-tp
  template-including-parent:: false
	- item-name???
	  tags:: PR, PR-pending
	  pr:: 
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