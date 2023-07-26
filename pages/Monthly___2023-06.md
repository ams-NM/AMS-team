filters:: {"monthly" false}

- [Last Month]([[Monthly/2023-05]]) << | >> [Next Month]([[Monthly/2023-07]])
- ## 📌Outstanding
	- [[🐞CM -GP Failed After Lightning Strike]]
- ## DONE Misc
  collapsed:: true
	- [[Competency Test Plan for NM RC Shift Staffs]]
	- [[AWOS]] drill, found [[Backup Wind]] PC display blank. - [[2023-06-26 Mon]]
		- The PC was on, but display showed no signal.
		- Rebooted the PC, and found that the mouse was not working properly.
		- Unplugged the 485-to-232 adapter which connects to a  PCIe-to-COM module.
		- Then reboot the PC again, re-plugged the 485-232 adapter, open the [[Vaisala]] software, [[Backup Wind]] data showed normally.
	- [[Vaisala]] engineer came visiting sensors along RWY. -[[2023-06-26 Mon]]
	- DONE 🛠️Fasten loose cables along `RWY`
	  done:: #{"{"}
	  plan:: [[2023-06-26 Mon]] 
	  finished::
	  remark:: AWOS & DVOR
	- spare MOXA port server for new [[AWOS]] 
	  done:: #{"{"}
	  plan::
	  finished::
	  remark:: Found  a spare one. We can then buy it from [[Vaisala]]
		- https://www.moxa.com/en/products/industrial-edge-connectivity/serial-device-servers/industrial-device-servers/nport-ia5000a-series/nport-ia5150a
		- https://us.rs-online.com/product/moxa/nport-ia5150a/71992227/
	- DONE Post [[Blackball]] & [[Thunderstorm]] check
	  done:: #{"{"}
	  plan:: [[2023-06-07 Wed]] 
	  finished:: [[2023-06-07 Wed]] 
	  remark::
	- DONE [[CTM]] came replacing MODEM connecting to workstation on SMG Headquarter.
	  done:: #{"{"}
	  plan:: [[2023-06-06 Tue]] 
	  finished::
	  remark:: The connection to SMG PC resumed the next day.
	- [[🐞CM -GP Failed After Lightning Strike]]
	- ➡️ [[NM New Staff Training]] 
	  done:: #{"{"}
	  plan:: 
	  remark:: prepare content, make schedule
	  finished::
	- SMG NEW AWOS data link to SMG Headquarter, to use [[MOXA Port Server]] `NET13` 
	  done:: #{"{"}
	  plan:: 
	  remark:: Waiting for reschedule
	  finished::
		- Old AWOS: Data comes from the single port server. New AWOS uses multiple port servers for different equipment. SMG needs to modify their implementation?
			- Use new [[MOXA Port Server]] of ==NET13==, which configured to output all weather data to a RS232 port. Confirmed by [[Vaisala]] Beijing Engineer. Test on a laptop by SMG staff on [[2023-06-27 Tue]]
		- They changed schedule, was [[2023-03-13 Mon]]
	- ➡️ [[VCS]] printer cartridge 
	  done:: #{"{"}
	  plan::
	  finished::
	  remark::
	- DONE [[AWOS]] printer cartridge 
	  done:: #{"{"}
	  plan:: [[2023-06-27 Tue]] 
	  finished:: [[2023-06-27 Tue]] 
	  remark:: [[Eric]] sent request to [[Susanna]]
	- ➡️ Buy capacitor for [[LT31]] blower,  2μF
	  done:: #{"{"}
	  plan::
	  remark:: RS: 196-4731
	  finished::
		- ```
		  - https://hken.rs-online.com/web/p/film-capacitors/1964731
		  - https://hken.rs-online.com/web/p/film-capacitors/1728179
		  - https://hken.rs-online.com/web/p/film-capacitors/3887664
		  ```
	- DONE [[Sub Station 5]] 30-min interruption during 3:00 - 7:00 am 
	  done:: #{"{"}
	  plan:: [[2023-06-07 Wed]] 
	  finished:: [[2023-06-07 Wed]] 
	  remark:: Postponed from [[2023-06-02 Fri]]
	- ➡️ Replace LT31 [[RWY-MID]]  Tx, Rx & Blowers
	  done:: #{"{"}
	  plan:: [[2023-07-03 Mon]] 
	  finished::
	  remark:: Replace LTM111 & LTM211 as well. From 2023-04
		- DONE LT31 Blower's capacitor power adapter cord replacement in advanced
		  done:: #{"{"}
		  plan:: [[2023-05-24 Wed]] 
		  finished:: [[2023-05-24 Wed]] 
		  remark:: 2 spare in GP done already. Brought 1 back and install a used capacitor on it with a power cord with the easy replacing adapter cord.
		- DONE Make Sure [[LT31]] Both Tx & Rx Units are present
		  done:: #{"{"}
		  plan:: [[2023-05-15 Mon]] 
		  finished:: [[2023-05-16 Tue]] 
		  remark:: 2 Rx in GP. 1 Tx (LTM112) in ATC warehouse
	- ➡️ Replace [[PWD]] [[RWY34]] 
	  done:: #{"{"}
	  plan:: [[2023-07-03 Mon]] 
	  finished::
	  remark:: Postponed due to `Platform Truck` oil leaking.
		- The cause: `CAL command` Ignored
		- [[AWOS]]-6m, [[PWD Calibration]]
	- DONE [[PTB]] [[RWY16]] due for ==Calibration==
	  done:: #{"{"}
	  plan:: [[2023-06-07 Wed]] 
	  finished:: [[2023-06-07 Wed]] 
	  remark::
- ## DONE Weekly PM
	- DONE `W05` [[ILS]] Weekly ,  Site Visit
	  done:: #{"{"}
	  plan:: [[2023-06-29 Thu]] 
	  finished:: [[2023-06-29 Thu]] 
	  remark::
	- DONE `W05` [[ILS]] Weekly,  Monitor Printouts 
	  done:: #{"{"}
	  plan:: [[2023-06-27 Tue]] 
	  finished:: [[2023-06-27 Tue]] 
	  remark::
	- DONE `W05` [[VCS]] Weekly ,  History Logs 
	  done:: #{"{"}
	  plan:: [[2023-06-27 Tue]] 
	  finished:: [[2023-06-27 Tue]] 
	  remark::
	- DONE `W05` [[Monday Routines]] 
	  done:: #{"{"}
	  plan:: [[2023-06-26 Mon]] 
	  finished::
	  remark::
	- DONE `W04` [[ILS]] Weekly,  Site Visit 
	  done:: #{"{"}
	  plan:: [[2023-06-19 Mon]] 
	  finished:: [[2023-06-19 Mon]] 
	  remark::
	- DONE `W04` [[ILS]] Weekly,  Monitor Printouts 
	  done:: #{"{"}
	  plan:: [[2023-06-23 Fri]] 
	  finished:: [[2023-06-23 Fri]] 
	  remark::
	- DONE `W04` [[VCS]] Weekly,  History Logs 
	  done:: #{"{"}
	  plan:: [[2023-06-23 Fri]] 
	  finished:: [[2023-06-23 Fri]] 
	  remark::
	- DONE `W04` [[Monday Routines]] 
	  done:: #{"{"}
	  plan:: [[2023-06-19 Mon]] 
	  finished:: [[2023-06-19 Mon]] 
	  remark::
	- DONE `W03` [[ILS]] Weekly,  Site Visit 
	  done:: #{"{"}
	  plan:: [[2023-06-14 Wed]] 
	  finished::
	  remark::
	- DONE `W03` [[ILS]] Weekly,  Monitor Printouts 
	  done:: #{"{"}
	  plan:: [[2023-06-12 Mon]]
	  finished::
	  remark:: [[GP]] not fixed yet ; [[LLZ]] printout on [[2023-06-12 Mon]]
	- DONE `W03` [[VCS]] Weekly,  History Logs 
	  done:: #{"{"}
	  plan:: [[2023-06-16 Fri]] 
	  finished::
	  remark::
	- DONE `W03` [[Monday Routines]] 
	  done:: #{"{"}
	  plan:: [[2023-06-12 Mon]] 
	  finished:: [[2023-06-12 Mon]] 
	  remark::
	- DONE `W02` [[ILS]] Weekly,  Site Visit 
	  done:: #{"{"}
	  plan:: [[2023-06-07 Wed]] 
	  finished:: [[2023-06-07 Wed]] 
	  remark::
	- DONE `W02` [[ILS]] Weekly,  Monitor Printouts 
	  done:: #{"{"}
	  plan:: [[2023-06-05 Mon]] 
	  finished:: [[2023-06-05 Mon]] 
	  remark::
	- DONE `W02` [[VCS]] Weekly,  History Logs 
	  done:: #{"{"}
	  plan:: [[2023-06-06 Tue]] 
	  finished:: [[2023-06-06 Tue]] 
	  remark::
	- DONE `W02` [[Monday Routines]] 
	  done:: #{"{"}
	  plan:: [[2023-06-05 Mon]] 
	  finished:: [[2023-06-05 Mon]] 
	  remark::
	- DONE `W01` [[ILS]] Weekly,  Site Visit 
	  done:: #{"{"}
	  plan::
	  finished:: [[2023-05-31 Wed]] 
	  remark::
	- DONE `W01` [[ILS]] Weekly,  Monitor Printouts 
	  done:: #{"{"}
	  plan:: [[2023-06-02 Fri]] 
	  finished:: 
	  remark::
	- DONE `W01` [[VCS]] Weekly,  History Logs 
	  done:: #{"{"}
	  plan:: [[2023-06-02 Fri]] 
	  finished:: [[2023-06-02 Fri]] 
	  remark:: From [[Monthly/2023-05]]
- ## DONE Monthly PM
  collapsed:: true
	- DONE [[VCS]] monthly 
	  done:: #{"{"}
	  plan:: [[2023-06-07 Wed]] 
	  finished:: [[2023-06-07 Wed]] 
	  remark:: line check done [[2023-06-05 Mon]]
	- DONE [[IGS]] monthly 
	  done:: #{"{"}
	  plan:: [[2023-06-30 Fri]] 
	  finished:: [[2023-06-30 Fri]] 
	  remark:: Done on [[2023-06-14 Wed]]
	- DONE [[FA36]] monthly 
	  done:: #{"{"}
	  plan:: [[2023-06-28 Wed]] 
	  finished:: [[2023-06-28 Wed]] 
	  remark::
	- ### DONE [[ILS]] Monthly PM
		- DONE [[ILS]] Monthly, Record DC Voltages on site 
		  done:: #{"{"}
		  plan:: [[2023-06-07 Wed]] 
		  finished:: [[2023-06-07 Wed]] 
		  remark::
		- DONE [[ILS]] Monthly, LLZ Ground Check 
		  done:: #{"{"}
		  plan:: [[2023-06-12 Mon]] 
		  finished:: [[2023-06-12 Mon]] 
		  remark:: 11:00 ~ 12:00
		- DONE [[ILS]] Monthly, MIT & Shutdown Tests 
		  done:: #{"{"}
		  plan:: [[2023-06-19 Mon]] 
		  finished:: [[2023-06-19 Mon]] 
		  remark::
		- DONE [[ILS]] Monthly, ==Form== 
		  done:: #{"{"}
		  plan:: [[2023-06-29 Thu]] 
		  finished:: [[2023-06-29 Thu]] 
		  remark:: 4 hr
	- ### DONE [[DVOR]] Monthly PM
		- DONE [[DVOR]] Monthly, Site Visit
		  done:: #{"{"}
		  plan:: [[2023-06-07 Wed]] 
		  finished:: [[2023-06-07 Wed]] 
		  remark:: 0 hours
		- DONE [[DVOR]] Monthly, Changeover & Parameter Printouts
		  done:: #{"{"}
		  plan:: [[2023-06-13 Tue]] 
		  finished:: [[2023-06-13 Tue]] 
		  remark:: 4 x 4 hours
			- DONE 1. Parameter Printout -A
			- DONE 2. Changeover
			- DONE 3. Parameter Printout -B
			- DONE 4. Record DC Voltage on ADRACS
	- ### DONE [[AWOS]] Monthly PM
		- DONE [[AWOS]] Monthly, Windows Cleaning -Platform Truck🚛
		  done:: #{"{"}
		  plan:: [[2023-06-26 Mon]] 
		  finished:: [[2023-06-26 Mon]] 
		  remark:: Used [[Car Washer]] instead. Postponed due to oil leakage of the truck , was [[2023-06-23 Fri]]
		- DONE [[AWOS]] Monthly, Ground Equipment
		  done:: #{"{"}
		  plan:: [[2023-06-08 Thu]] 
		  finished:: [[2023-06-08 Thu]] 
		  remark:: AM, 4 x 4 hours
		- DONE [[AWOS]] Monthly, ==Form==
		  done:: #{"{"}
		  plan:: [[2023-06-30 Fri]] 
		  finished:: [[2023-06-30 Fri]] 
		  remark:: 4 x 4 hours
- ## DONE x-Monthly Routines
- ## DONE TS
  collapsed:: true
	- DONE [[Site Cleaning]] (2nd Wednesday) 
	  done:: #{"{"}
	  plan:: [[2023-06-14 Wed]] 
	  finished::
	  remark::
	- DONE Workplace Safety -ISO45001 `FCOHSP 9.1.1-03`
	  done:: #{"{"}
	  plan:: [[2023-06-28 Wed]] 
	  finished:: [[2023-06-28 Wed]] 
	  remark::
## TODO End of Month - [[Email]]
collapsed:: true
	- DONE [[Review CM Status]]
	  plan:: [[2023-07-03 Mon]] 
	  finished::
	  remark::
		- DONE Verify `Failure Code` is present on every CM.
	- TODO [[PM Monthly Schedule to AOD]] 
	  done:: #{"{"}
	  plan::
	  finished::
	  remark::
- ## DONE Start of Month
  collapsed:: true
	- DONE Verify `AWOS` daily backup logs. (Soft link on maintenance PC to TCD workstation)
	- DONE Check `PM Incomplete from Last Month` on Maximo
	- DONE Complete PM last month
	- DONE Complete TS las month
	- DONE Complete CM
	- DONE Initiate PM (Choose multiple W.O. -> "Select Records")
	- DONE Arrange Dates for PMs of The Month
- ## Future Issues (To move over)
	-
## Members Absent
	- DONE [[Eric]] on [[AL]] 
	  done:: #{"{"}
	  plan:: [[2023-06-06 Tue]] 
	  finished::
	  remark::
	- DONE [[Eric]] on [[al]] 
	  done:: #{"{"}
	  plan:: [[2023-06-05 Mon]] 
	  finished::
	  remark::
	- DONE [[Aaron]] on [[CL]] 
	  done:: #{"{"}
	  plan:: [[2023-06-09 Fri]] 
	  finished::
	  remark:: Compensates last Saturday worked on [[🐞CM -GP Failed After Lightning Strike]]
	- DONE [[Aaron]] on [[AL]] 
	  done:: #{"{"}
	  plan:: [[2023-06-16 Fri]] 
	  finished::
	  remark::
	- DONE [[Nick]] on AM [[AL]] 
	  done:: #{"{"}
	  plan:: [[2023-06-16 Fri]] 
	  finished::
	  remark::