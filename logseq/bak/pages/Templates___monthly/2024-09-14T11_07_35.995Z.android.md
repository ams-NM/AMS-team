type:: templates

- ## Monthly Schedule Page Template
  template:: monthly-tp
  template-including-parent:: false
	- [Last Month]([[Monthly/]]) << | >> [Next Month]([[Monthly/]])
	- ## 📌Outstanding
	- ## Tasks and Issues of the Month {{renderer :todomaster}}
		-
	- ## Weekly PM {{renderer :todomaster}}
	  collapsed:: true
		- TODO  `W05` ==Weekly PM Plan==
		  done:: #{"{"}
		  plan::
		- TODO `W05` [[ILS]] Weekly ,  🏠️Site Visit
		  done:: #{"{"}
		  plan::
		- TODO `W05` [[ILS]] Weekly, 📄Monitor Printouts 
		  done:: #{"{"}
		  plan::
		- TODO `W05` [[VCS]] Weekly
		  done:: #{"{"}
		  plan::
		- TODO `W05` [[Monday Routines]] 
		  done:: #{"{"}
		  plan::
		- TODO  `W04` ==Weekly PM Plan==
		  done:: #{"{"}
		  plan::
		- TODO `W04` [[ILS]] Weekly, 🏠️Site Visit 
		  done:: #{"{"}
		  plan::
		- TODO `W04` [[ILS]] Weekly, 📄Monitor Printouts 
		  done:: #{"{"}
		  plan::
		- TODO `W04` [[VCS]] Weekly
		  done:: #{"{"}
		  plan::
		- TODO `W04` [[Monday Routines]] 
		  done:: #{"{"}
		  plan::
		- TODO  `W03` ==Weekly PM Plan==
		  done:: #{"{"}
		  plan::
		- TODO `W03` [[ILS]] Weekly, 🏠️Site Visit 
		  done:: #{"{"}
		  plan::
		- TODO `W03` [[ILS]] Weekly, 📄Monitor Printouts 
		  done:: #{"{"}
		  plan::
		- TODO `W03` [[VCS]] Weekly
		  done:: #{"{"}
		  plan::
		- TODO `W03` [[Monday Routines]] 
		  done:: #{"{"}
		  plan::
		- TODO  `W02` ==Weekly PM Plan==
		  done:: #{"{"}
		  plan::
		- TODO `W02` [[ILS]] Weekly, 🏠️Site Visit 
		  done:: #{"{"}
		  plan::
		- TODO `W02` [[ILS]] Weekly, 📄Monitor Printouts 
		  done:: #{"{"}
		  plan::
		- TODO `W02` [[VCS]] Weekly
		  done:: #{"{"}
		  plan::
		- TODO `W02` [[Monday Routines]] 
		  done:: #{"{"}
		  plan::
		- TODO  `W01` ==Weekly PM Plan==
		  done:: #{"{"}
		  plan::
		- TODO `W01` [[ILS]] Weekly, 🏠️Site Visit 
		  done:: #{"{"}
		  plan::
		- TODO `W01` [[ILS]] Weekly, 📄Monitor Printouts 
		  done:: #{"{"}
		  plan::
		- TODO `W01` [[VCS]] Weekly
		  done:: #{"{"}
		  plan::
		- TODO `W01` [[Monday Routines]] 
		  done:: #{"{"}
		  plan::
	- ## Monthly PM {{renderer :todomaster}}
		- ### [[VCS]] Monthly PM {{renderer :todomaster}}
		  labor:: 24 hours
			- TODO [[VCS]] monthly - 📞Line check & Save config
			  done:: #{"{"}
			  plan:: 
			  labor::  4 x 4 hours
			- TODO [[VCS]] monthly -==Form== 
			  done:: #{"{"}
			  plan:: 
			  labor::  2 x 4 hours
		- ### [[IGS]] Monthly PM {{renderer :todomaster}}
		  labor:: 32 hours
			- TODO [[IGS]] monthly PM - 🏠️Site
			  done:: #{"{"}
			  plan:: 
			  labor:: 4 x 4 hours
			- TODO [[IGS]] monthly -==From== 
			  done:: #{"{"}
			  plan:: 
			  labor::  4 x 4 hours
		- ### TODO [[FA36]] monthly 
		  done:: #{"{"}
		  plan:: 
		  labor:: 16 hours
		- ### [[ILS]] Monthly PM {{renderer :todomaster}}
		  labor:: 32 hours
		  collapsed:: true
			- TODO [[ILS]] Monthly, Record DC Voltages on site 
			  done:: #{"{"}
			  plan::
			- TODO [[ILS]]-m, Battery Voltages on site 
			  done:: #{"{"}
			  plan::
			  labor:: 1 x 4 hours
			- TODO [[ILS]] Monthly, LLZ Ground Check 
			  done:: #{"{"}
			  plan:: 
			  labor:: 4 x 4 hours
			- TODO [[ILS]] Monthly, MIT & Shutdown Tests 
			  done:: #{"{"}
			  plan:: 
			  labor:: 4 x 4 hours
			- TODO [[ILS]] -m, Sync Date/Time 
			  done:: #{"{"}
			  plan::
			- TODO [[ILS]] Monthly, ==Form== 
			  done:: #{"{"}
			  plan::
		- ### [[DVOR]] Monthly PM {{renderer :todomaster}}
		  labor:: 16 hours
			- TODO [[DVOR]] Monthly, Site Visit
			  done:: #{"{"}
			  plan::
			  labor:: 1 x 4 hours
			- TODO [[DVOR]] Monthly, Changeover & Parameter Printouts
			  done:: #{"{"}
			  plan::
			  labor:: 4 x 4 hours
				- TODO 1. Parameter Printout -A
				- TODO 2. Changeover
				- TODO 3. Parameter Printout -B
				- TODO 4. Record DC Voltage on ADRACS
		- ### [[AWOS]] Monthly PM {{renderer :todomaster}}
		  labor:: 48 hours
			- TODO [[AWOS]] Monthly, Windows Cleaning -Platform Truck🚛
			  done:: #{"{"}
			  plan:: 
			  laobr:: 4x 8 hours
			- TODO [[AWOS]] Monthly, Ground Equipment
			  done:: #{"{"}
			  plan::
			  labor:: 4 x 4 hours
			- TODO [[AWOS]] Monthly, ==Form== 
			  done:: #{"{"}
			  plan:: 
			  labor:: 4 x 4 hours
	- ## ❌-Monthly Routines {{renderer :todomaster}}
	  collapsed:: true
		- TODO Add 3-m, 6-m, yearly PMs, etc.
		- TODO incomplete PMs from previous months
	- ## TS {{renderer :todomaster}}
	  collapsed:: true
		- TODO [[Site Cleaning]] (2nd Wednesday) 
		  done:: #{"{"}
		  plan::
		- TODO Workplace Safety -ISO45001 `FCOHSP 9.1.1-03`
		  done:: #{"{"}
		  plan::
		- TODO Ladder & Tools Check `FCOHSP 9.1.1-04` (Odd Months) 
		  done:: #{"{"}
		  plan::
	- ## End of Month {{renderer :todomaster}}
	  collapsed:: true
		- TODO Generate PM schedule📅 for the coming month
		  done:: #{"{"}
		  plan::
		- TODO Check [[Calibration Records]] for next month
		  done:: #{"{"}
		  plan::
		- TODO [[Review CM Status]]
		  plan:: 
		  remark:: Verify `Failure Code` is present on every CM.
	- ## Start of Month {{renderer :todomaster}}
	  collapsed:: true
		- TODO Initialize ==Daily PMs== on [[Maximo]]
		- TODO Verify `AWOS` daily backup logs. (Soft link on maintenance PC to TCD workstation)
		- TODO Check `PM Incomplete from Last Month` on Maximo
		- TODO Complete PM last month
		- TODO Complete TS las month
		- TODO Complete CM
		- TODO Initiate PM (Choose multiple W.O. -> "Select Records")
		- TODO Arrange Dates for PMs of The Month
		-
	- ## Future Issues (To move over)
		-
	- ## Members Absent
		-