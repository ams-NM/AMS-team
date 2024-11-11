type:: templates

- ## Monthly Schedule Page Template
  template:: monthly-tp
  template-including-parent:: false
	- [Last Month]([[Monthly/]]) << | >> [Next Month]([[Monthly/]])
	- ## 📌Outstanding {{renderer :todomaster}}
	- ## Tasks and Issues of the Month {{renderer :todomaster}}
		-
	- ## Weekly PM {{renderer :todomaster}}
		- TODO [[Monday Routines]] #w01 #aaron 
		  done:: #{"{"}
		  date::
		- TODO [[ILS]] `Weekly`, 📄Monitor Printouts #w01
		  date::
		- TODO [[VCS]] `Weekly` #w01
		  date::
		- TODO [[ILS]] `Weekly` ,  🏠️Site Visit #w01
		  done:: #{"{"}
		  date::
		- TODO  ==Weekly PM Plan== #w01 #aaron 
		  date::
		- TODO [[Monday Routines]] #w02 #aaron 
		  done:: #{"{"}
		  date::
		- TODO  [[ILS]] `Weekly`, 📄Monitor Printouts  #w02
		  date::
		- TODO  [[VCS]] `Weekly` #w02
		  date::
		- TODO  [[ILS]] `Weekly` ,  🏠️Site Visit #w02
		  done:: #{"{"}
		  date::
		- TODO  ^^Weekly PM Plan^^ #w02 #aaron 
		  date::
		- TODO [[Monday Routines]] #w03 #aaron 
		  done:: #{"{"}
		  date::
		- TODO [[ILS]] `Weekly`, 📄Monitor Printouts #w03 
		  date::
		- TODO [[VCS]] `Weekly` #w03
		  date::
		- TODO [[ILS]] `Weekly` ,  🏠️Site Visit #w03
		  done:: #{"{"}
		  date::
		- TODO ^^Weekly PM Plan^^ #w03 #aaron 
		  date::
		- TODO [[Monday Routines]] #w04 #aaron 
		  done:: #{"{"}
		  date::
		- TODO [[ILS]] `Weekly`, 📄Monitor Printouts #w04
		  date::
		- TODO [[VCS]] `Weekly` #w04
		  date::
		- TODO [[ILS]] `Weekly` ,  🏠️Site Visit #w04
		  done:: #{"{"}
		  date::
		- TODO ^^Weekly PM Plan^^ #w04 #aaron 
		  date::
		- TODO [[Monday Routines]] #w05 #aaron 
		  done:: #{"{"}
		  date::
		- TODO [[ILS]] `Weekly`, 📄Monitor Printouts #w05 
		  date::
		- TODO [[VCS]] `Weekly` #w05
		  date::
		- TODO [[ILS]] `Weekly` ,  🏠️Site Visit #w05
		  done:: #{"{"}
		  date::
		- TODO ^^Weekly PM Plan^^ #w05 #aaron 
		  date::
	- ## Monthly PM {{renderer :todomaster}}
	  collapsed:: true
		- ### [[VCS]] Monthly PM {{renderer :todomaster}}
		  labor:: 24 hours
			- TODO [[VCS]] `Monthly` - 📞Line check & Save config
			  done:: #{"{"}
			  date:: 
			  labor::  4 x 4 hours
			- TODO [[VCS]] `Monthly` -==Form== 
			  done:: #{"{"}
			  date:: 
			  labor::  2 x 4 hours
		- ### [[IGS]] Monthly PM {{renderer :todomaster}}
		  labor:: 32 hours
			- TODO [[IGS]] `Monthly` PM - 🏠️Site
			  done:: #{"{"}
			  date:: 
			  labor:: 4 x 4 hours
			- TODO [[IGS]] `Monthly` -==From== 
			  done:: #{"{"}
			  date:: 
			  labor::  4 x 4 hours
		- ### TODO [[FA36]] monthly 
		  done:: #{"{"}
		  date:: 
		  labor:: 16 hours
		- ### [[ILS]] Monthly PM {{renderer :todomaster}}
		  labor:: 32 hours
			- TODO [[ILS]] -`Monthly`, Record DC Voltages on site 
			  done:: #{"{"}
			  date::
			- TODO [[ILS]]-`Monthly`, Battery Voltages on site 
			  done:: #{"{"}
			  date::
			  labor:: 1 x 4 hours
			- TODO [[ILS]] `Monthly`, LLZ Ground Check 
			  done:: #{"{"}
			  date:: 
			  labor:: 4 x 4 hours
			- TODO [[ILS]] `Monthly`, MIT & Shutdown Tests 
			  done:: #{"{"}
			  date:: 
			  labor:: 4 x 4 hours
			- TODO [[ILS]] -`Monthly`, Sync Date/Time on `RCSE` 
			  done:: #{"{"}
			  date::
			- TODO [[ILS]] `Monthly`, ==Form== 
			  done:: #{"{"}
			  date::
		- ### [[DVOR]] Monthly PM {{renderer :todomaster}}
		  labor:: 16 hours
			- TODO [[DVOR]] `Monthly`, Site Visit
			  done:: #{"{"}
			  date::
			  labor:: 1 x 4 hours
			- TODO [[DVOR]] `Monthly`, Changeover & Parameter Printouts
			  done:: #{"{"}
			  date::
			  labor:: 4 x 4 hours
				- TODO 1. Parameter Printout -A
				- TODO 2. Changeover
				- TODO 3. Parameter Printout -B
				- TODO 4. Record DC Voltage on ADRACS
		- ### [[AWOS]] Monthly PM {{renderer :todomaster}}
		  labor:: 48 hours
			- TODO [[AWOS]] `Monthly`, Windows Cleaning -Platform Truck🚛
			  done:: #{"{"}
			  date:: 
			  laobr:: 4x 8 hours
			- TODO [[AWOS]] `Monthly`, Ground Equipment
			  done:: #{"{"}
			  date::
			  labor:: 4 x 4 hours
			- TODO [[AWOS]] `Monthly`, ==Form== 
			  done:: #{"{"}
			  date:: 
			  labor:: 4 x 4 hours
	- ## ❌-Monthly Routines {{renderer :todomaster}}
	  collapsed:: true
		- TODO Add 3-m, 6-m, yearly PMs, etc.
		- TODO incomplete PMs from previous months
	- ## TS {{renderer :todomaster}}
		- TODO [[Site Cleaning]] (2nd Wednesday) 
		  done:: #{"{"}
		  date::
		- TODO ⛑️Workplace Safety -ISO45001 `FCOHSP 9.1.1-03`
		  done:: #{"{"}
		  date::
		- TODO 🪜Ladder & Tools Check `FCOHSP 9.1.1-04` (==Odd Months Only==) 
		  done:: #{"{"}
		  date::
	- ## End of Month {{renderer :todomaster}}
		- TODO Generate PM schedule📅 for the coming month
		  done:: #{"{"}
		- TODO Check [[Calibration Records]] for next month
		  done:: #{"{"}
		- TODO [[Review CM Status]]
		  
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
	- ## Future Issues (==To move over==)
	- ## Members Absent {{renderer :todomaster}}
	- ## [[Maximo]] Labor Data
	  collapsed:: true
		- ### All `TECHS` records (template name: `special-labor-tp`)
			- TODO Technical Service
			  date:: 
			  tags:: labor-todo
			  wo:: TECHS
			  time:: 4 hours
			  staffs:: [[All-staffs]]
		- {{renderer :smartblock, labor-query-tp, Click to create labor view (Remove this Block AFTER use), true}}