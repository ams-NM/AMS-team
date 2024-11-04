- [Last Month]([[Monthly/2024-09]]) << | >> [Next Month]([[Monthly/2024-11]])
- ## 📌Outstanding {{renderer :todomaster}}
  collapsed:: true
	- ((66fe3a25-0e9c-4ac9-8d4b-157a02f45fb4))
		- [[ILS Calibration & Normalization]] ==Failed== on [[GP]] `CRS Width`
		  wo:: 652863
		  date:: [[2024-10-23 Wed]]
		  collapsed:: true
			- The monitor readings of `CRS Width DDM` had been shifted to the upper end for a long time
				- Tx1: 18.9 ~ 19.0%, Tx2: 18.0 ~ 18.1%.
				- Nominal value: 17.5%
			- So we planed to do [[calibrate and normalize]] to correct them.
			- After [[Flight Check]] on [[ILS]], we accessed this feature on [[ADRACS]] software, and click 'calibrate', then 'normalize` with Tx2 on air.
				- The `RF Level` and `SDM` were changed to nominal values, but not the `DDM`. It shifted from 18.0 to 18.5%
				- And all three parameters were in Alarm state, with `Monitor BITE` alarm as well.
				- In order to clear the alarms, we tried `reboot` on the software, PC, [[GP]]... But nothing changed.
			- [[Eric]] asked his teacher in previous course. He suggested us to change the nominal value and make it close to what the monitor readings were, and then did [[calibrate and normalize]]. We did it step by step, changed to 18.3%, [[calibrate and normalize]] succeeded. And then 18.0%, and 17.8%. But it failed again when we tried a value lower than `17.8%`.
			- [[Stanley]] suggested to tune the [[SOAC]], then it resumed normal
				- We went back to retrieve the [[Scope]]
				- According too the manual, adjusted the `CRS Width` path and make the reading of monitors to be close to nominal values.
				- Then [[calibrate and normalize]] succeeded with nominal DDM on `17.5%`.
			-
	- ((66fe3a26-87b7-482a-ace2-f54e0aa54564))
- ## Tasks and Issues of the Month {{renderer :todomaster}}
  collapsed:: true
	- DONE Complete [[ATC]] [[VCS Console]] button removal TS #aaron 
	  date:: [[2024-10-04 Fri]]
		- DONE Prepare connector on [[2024-08-08 Thu]]
	- TODO 接線段子和壓線鉗 for [[VCS Console]] PSU 
	  tags:: IMO, IMO-pending
	  wo:: 648475
	  issued:: [[2024-10-09 Wed]]
	  received::
	- TODO Wago 2P plugs, 10 pcs for [[VCS Console]] PSU
	  tags:: IMO, IMO-pending
	  wo:: 648475
	  issued:: [[2024-10-09 Wed]]
	  received::
- ## Weekly PM {{renderer :todomaster}}
  collapsed:: true
	- DONE  `W01` ==Weekly PM Plan== #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-03 Thu]]
	- DONE `W01` [[VCS]] Weekly
	  date:: [[2024-10-04 Fri]]
	  tags:: labor-todo
	  wo:: 650083
	  time:: 1400-1800
	  staffs:: [[Aaron]], [[Eric]], [[Nick]]
	- DONE `W01` [[ILS]] Weekly ,  🏠️Site Visit
	  done:: #{"{"}
	  date:: [[2024-10-03 Thu]]
	  tags:: labor-todo
	  wo:: 647317 
	  time:: 0900-1300
	  staffs:: [[All-staffs]]
	- DONE `W01` [[Monday Routines]] #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-03 Thu]]
	- DONE  `W02` ==Weekly PM Plan==  #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-10 Thu]]
	- DONE `W02` [[ILS]] Weekly, 🏠️Site Visit 
	  done:: #{"{"}
	  date:: [[2024-10-09 Wed]]
	  tags:: labor-todo
	  wo:: 650046
	  time:: 0900-1300
	  staffs:: [[Nick]]
	- DONE `W02` [[ILS]] Weekly, 📄Monitor Printouts 
	  done:: #{"{"}
	  date:: [[2024-10-07 Mon]]
	  tags:: labor-todo
	  wo:: 650046
	  time:: 0900-1300
	  staffs:: [[Aaron]], [[Eric]], [[Nick]]
	- DONE `W02` [[VCS]] Weekly
	  done:: #{"{"}
	  date:: [[2024-10-08 Tue]]
	  tags:: labor-todo
	  wo:: 650084
	  time:: 1400-1800
	  staffs:: [[All-staffs]]
	- DONE `W02` [[Monday Routines]]  #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-07 Mon]]
	- DONE  `W03` ==Weekly PM Plan== #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-17 Thu]]
	- DONE `W03` [[ILS]] Weekly, 🏠️Site Visit 
	  done:: #{"{"}
	  date:: [[2024-10-16 Wed]]
	  tags:: labor-todo
	  wo:: 650047
	  time:: 0900-1300
	  staffs:: [[Nick]]
	- DONE `W03` [[ILS]] Weekly, 📄Monitor Printouts 
	  done:: #{"{"}
	  date:: [[2024-10-15 Tue]]
	  tags:: labor-todo
	  wo:: 650047
	  time:: 1400-1800
	  staffs:: [[Aaron]], [[Eric]], [[Vincent]]
	- DONE `W03` [[VCS]] Weekly
	  done:: #{"{"}
	  date:: [[2024-10-15 Tue]]
	  tags:: labor-todo
	  wo:: 650085
	  time:: 0900-1300
	  staffs:: [[Aaron]], [[Eric]], [[Vincent]]
	- DONE `W03` [[Monday Routines]]  #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-14 Mon]]
	- DONE  `W04` ==Weekly PM Plan==  #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-24 Thu]]
	- DONE `W04` [[ILS]] Weekly, 🏠️Site Visit 
	  done:: #{"{"}
	  date:: [[2024-10-23 Wed]]
	- DONE `W04` [[ILS]] Weekly, 📄Monitor Printouts 
	  done:: #{"{"}
	  date:: [[2024-10-21 Mon]]
	- DONE `W04` [[VCS]] Weekly
	  done:: #{"{"}
	  date:: [[2024-10-24 Thu]]
	- DONE `W04` [[Monday Routines]]  #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-21 Mon]]
	- DONE `W05` [[VCS]] Weekly
	  done:: #{"{"}
	  date:: [[2024-10-29 Tue]]
	- DONE  `W05` ==Weekly PM Plan== #aaron 
	  done:: #{"{"}
	  date:: [[2024-10-30 Wed]]
	- DONE `W05` [[ILS]] Weekly, 🏠️Site Visit 
	  done:: #{"{"}
	  date:: [[2024-10-30 Wed]]
	- DONE `W05` [[ILS]] Weekly, 📄Monitor Printouts 
	  done:: #{"{"}
	  date:: [[2024-10-28 Mon]]
	- DONE `W05` [[Monday Routines]]  #aaron
	  done:: #{"{"}
	  date:: [[2024-10-28 Mon]]
- ## Monthly PM {{renderer :todomaster}}
  collapsed:: true
	- ### [[VCS]] Monthly PM {{renderer :todomaster}}
	  labor:: 24 hours
		- DONE [[VCS]] monthly - 📞Line check & Save config
		  done:: #{"{"}
		  date:: [[2024-10-03 Thu]]
		  labor::  4 x 4 hours
		  tags:: labor-todo
		  wo:: 650088
		  time:: 1400-1800
		  staffs:: [[All-staffs]]
		- DONE [[VCS]] monthly -==Form== 
		  done:: #{"{"}
		  date:: [[2024-10-04 Fri]]
		  labor::  2 x 4 hours
		  tags:: labor-todo
		  wo:: 650088
		  time:: 0900-1300
		  staffs:: [[All-staffs]]
	- ### [[IGS]] Monthly PM {{renderer :todomaster}}
	  labor:: 32 hours
		- DONE [[IGS]] monthly PM - 🏠️Site
		  done:: #{"{"}
		  date:: [[2024-10-09 Wed]]
		  labor:: 4 x 4 hours
		  tags:: labor-todo
		  wo:: 649940
		  time:: 0900-1300
		  staffs:: [[Aaron]]
		- DONE [[IGS]] monthly -==From== 
		  done:: #{"{"}
		  id:: 66ff5f43-f7f9-478b-8b17-e844e684736e
		  date:: [[2024-10-09 Wed]]
		  labor:: 4 x 4 hours
		  tags:: labor-todo
		  wo:: 649940
		  time:: 1400-1800
		  staffs:: [[All-staffs]]
	- ### DONE [[FA36]] monthly 
	  done:: #{"{"}
	  date:: [[2024-10-28 Mon]] 
	  labor:: 16 hours
	- ### [[ILS]] Monthly PM {{renderer :todomaster}}
	  labor:: 32 hours
		- DONE [[ILS]] -m, Record DC Voltages on site 
		  done:: #{"{"}
		  date:: [[2024-10-23 Wed]]
		- DONE [[ILS]]-m, Battery Voltages on site 
		  done:: #{"{"}
		  date:: [[2024-10-15 Tue]]
		  labor:: 1 x 4 hours
		- DONE [[ILS]] Monthly, LLZ Ground Check 
		  done:: #{"{"}
		  date:: [[2024-10-14 Mon]]
		  labor:: 4 x 4 hours
		  tags:: labor-todo
		  wo::  650050
		  time:: 0600-0800
		  staffs:: [[Aaron]], [[Eric]], [[Vincent]]
		- DONE [[ILS]] Monthly, MIT & Shutdown Tests 
		  done:: #{"{"}
		  date:: [[2024-10-14 Mon]]
		  labor:: 4 x 4 hours
		- DONE [[ILS]] -m, Sync Date/Time on `RCSE` 
		  done:: #{"{"}
		  date:: [[2024-10-17 Thu]]
		- DONE [[ILS]] Monthly, ==Form== 
		  done:: #{"{"}
		  date:: [[2024-10-25 Fri]]
	- ### [[DVOR]] Monthly PM {{renderer :todomaster}}
	  labor:: 16 hours
		- DONE [[DVOR]] Monthly, Site Visit
		  done:: #{"{"}
		  date:: [[2024-10-14 Mon]]
		  labor:: 1 x 4 hours
		- DONE [[DVOR]] Monthly, Changeover & Parameter Printouts
		  done:: #{"{"}
		  date:: [[2024-10-17 Thu]]
		  labor:: 4 x 4 hours
			- DONE 1. Parameter Printout -A
			- DONE 2. Changeover on [[2024-10-14 Mon]]
			- DONE 3. Parameter Printout -B
			- DONE 4. Record DC Voltage on ADRACS
	- ### [[AWOS]] Monthly PM {{renderer :todomaster}}
	  labor:: 48 hours
		- DONE [[AWOS]] Monthly, Windows Cleaning -Platform Truck🚛
		  done:: #{"{"}
		  date:: [[2024-10-16 Wed]]
		  laobr:: 4x 8 hours
		- DONE [[AWOS]] Monthly, Ground Equipment
		  done:: #{"{"}
		  date:: [[2024-10-10 Thu]]
		  tags:: labor-todo
		  wo::  649358
		  time:: 0900-1300
		  staffs:: [[All-staffs]]
		  labor:: 4 x 4 hours
		- DONE [[AWOS]] Monthly, ==Form== 
		  done:: #{"{"}
		  date:: [[2024-10-25 Fri]]
		  labor:: 4 x 4 hours
- ## ❌-Monthly Routines {{renderer :todomaster}}
  collapsed:: true
	- ### [[Flight Check]] [[ILS]] {{renderer :todomaster}}
	  id:: 66fe3a25-0e9c-4ac9-8d4b-157a02f45fb4
		- DONE [[✈️Flight Check]] ==Pre== `meeting` at ==10:30==
		  date:: [[2024-10-18 Fri]]
		- DONE ✈️Flight Check [[ILS]] ==Pre== 
		  done:: #{"{"}
		  date:: [[2024-10-10 Thu]]
		  tags:: labor-todo
		  wo:: 651313
		  time:: 1400-1800
		  staffs:: [[All-staffs]]
		- DONE ✈️Flight Check [[ILS]] ==Pre== Connect FiberLink `LLZ` to `GP` 
		  done:: #{"{"}
		  date:: [[2024-10-16 Wed]]
		- DONE ✈️Flight Check [[ILS]] ==In-progress==
		  done:: #{"{"}
		  date:: [[2024-10-22 Tue]]
		  remark:: ends on [[2024-10-23 Wed]]
			- [[ILS Calibration & Normalization]]
				- Alarm activated after [[ILS Calibration & Normalization]] on [[GP]] `CRS Width`.
				- Refer CM `652863`
			- DONE [[LOC]] [[CLR]] RF power Tx1, change from ==7.1w to 7.2w==
			  date:: [[2024-10-22 Tue]]
				- Monitor reading: `15.x` -> `16.y`. But they went back to `13.x` at the end of F.C.
					- Probably because the temperature rises after sunrise.
			- DONE [[GP]] Tx2 `2.96°`, raise ==CSB1 DDM== setting
			  date:: [[2024-10-23 Wed]]
				- Change [[GP]] Tx2 ==CSB1 DDM== from `-11.80` to `-11.70`, F.C. result from `2.96` to `2.97`
		- DONE ✈️Flight Check [[ILS]] ==Post==, Param Printout Tx-A, Tx2
		  done:: #{"{"}
		  date:: [[2024-10-28 Mon]]
		- TODO ✈️Flight Check [[ILS]] ==Post==, Param Printout Tx-B 
		  done:: #{"{"}
		  date::
		- TODO ✈️Flight Check [[ILS]] ==Post==, LLZ Ground Check Points
		  done:: #{"{"}
		  date::
		- TODO ✈️Flight Check [[ILS]] ==Form== 
		  done:: #{"{"}
		  date::
		- TODO ✈️Flight Check [[ILS]] ^^Post^^, record `modifications` on Tx or Monitors
		  done:: #{"{"}
		  date::
			- TODO Record modifications on [[Maximo]] workorder
			- TODO Record modifications here ➡️ ((672042c2-2211-4a07-a55a-9c8f793c3951))
	- ### [[Flight Check]] [[DVOR]] {{renderer :todomaster}}
	  id:: 66fe3a26-87b7-482a-ace2-f54e0aa54564
		- DONE ✈️Flight Check [[DVOR]] ==In-progress==
		  done:: #{"{"}
		  date:: [[2024-10-24 Thu]]
		- DONE ✈️Flight Check [[DVOR]] ==Post==, Param Printout Tx-A 
		  done:: #{"{"}
		  date:: [[2024-10-31 Thu]]
		- TODO ✈️Flight Check [[DVOR]] ^^Post^^, Param Printout Tx-B
		  done:: #{"{"}
		  date:: [[2024-11-14 Thu]]
		- TODO ✈️Flight Check [[DVOR]] ^^Post^^, record `modifications` on Tx or Monitors
		  done:: #{"{"}
		  date::
			- TODO Record modifications on [[Maximo]] workorder
			- TODO Record modifications here ➡️ ((672042c2-2211-4a07-a55a-9c8f793c3951))
	- ### [[AWOS]] 3-Monthly PM {{renderer :todomaster}}
	  labor:: 48 hours
	  wo:: 649359
		- DONE [[AWOS]]-3m, [[ATIS Changeover -Steps]] 
		  done:: #{"{"}
		  date:: [[2024-10-24 Thu]]
			- Ask [[Tower]] for 5 min interruption
			  logseq.order-list-type:: number
			- `Make sure Ident & message are sync correctly on standby, before stopping the active one`
			  logseq.order-list-type:: number
			- After `changeover`, make sure both PC are working fine.
			  logseq.order-list-type:: number
			- Reboot ==standby== PC.
			  logseq.order-list-type:: number
		- DONE [[AWOS]]-3m, Workstation Disk Storage Check
		  done:: #{"{"}
		  date:: [[2024-10-07 Mon]]
		  tags:: labor-todo
		  wo:: 649359
		  time:: 1400-1800
		  staffs:: [[Eric]]
		- DONE [[AWOS]]-3m, ==Form==
		  done:: #{"{"}
		  date:: [[2024-10-24 Thu]]
	- ### [[AWOS]] 6-Monthly PM {{renderer :todomaster}}
	  labor:: 48 hours
		- DONE [[AWOS]]-6m, LT31 Calibration
		  done:: #{"{"}
		  date:: [[2024-10-16 Wed]]
		- DONE [[AWOS]]-6m, PWD Calibration
		  done:: #{"{"}
		  date:: [[2024-10-16 Wed]]
		- DONE [[AWOS]]-6m, ==Form==
		  done:: #{"{"}
		  date:: [[2024-10-29 Tue]]
	- ### [[DVOR]] 6-Monthly PM from [[Monthly/2024-09]] {{renderer :todomaster}}
	  labor:: 48 hours
	  collapsed:: true
		- {{embed ((66f22127-81ec-4d5d-a781-6a35162ee89e))}}
		- {{embed ((66ff5f42-431b-4dce-a081-e8887445306b))}}
	- ### [[DVOR]] Yearly PM from [[Monthly/2024-09]] {{renderer :todomaster}}
	  collapsed:: true
		- {{embed ((66f22127-0f31-4ed0-abae-21591a4f033e))}}
		- {{embed ((66ff5f42-f87d-4d14-ba52-ac7144d0bcf8))}}
- ## TS {{renderer :todomaster}}
  collapsed:: true
	- DONE [[Site Cleaning]] (2nd Wednesday) 
	  done:: #{"{"}
	  date:: [[2024-10-09 Wed]]
	  tags:: labor-todo
	  wo:: 629857
	  time:: 0900-1300
	  staffs:: [[Vincent]]
	- DONE ⛑️Workplace Safety -ISO45001 `FCOHSP 9.1.1-03`
	  done:: #{"{"}
	  date:: [[2024-10-17 Thu]]
- ## End of Month {{renderer :todomaster}}
  collapsed:: true
	- DONE Generate PM schedule📅 for the coming month
	  done:: #{"{"}
	- DONE Check [[Calibration Records]] for next month
	  done:: #{"{"}
	- DONE [[Review CM Status]] #aaron
	  date:: [[2024-10-30 Wed]]
	  remark:: Verify `Failure Code` is present on every CM.
- ## Start of Month {{renderer :todomaster}}
  collapsed:: true
	- DONE Initialize ==Daily PMs== on [[Maximo]]
	- DONE Verify `AWOS` daily backup logs. (Soft link on maintenance PC to TCD workstation)
		- Missing:
			- 01
			- 03, done at 08:22(LT) which was next shift
	- DONE Check `PM Incomplete from Last Month` on Maximo
	- DONE Complete PM last month
	- DONE Complete TS las month
	- DONE Complete CM
	- DONE Initiate PM (Choose multiple W.O. -> "Select Records")
	- DONE Arrange Dates for PMs of The Month
- ## Future Issues (==To move over==)
- ## Members Absent {{renderer :todomaster}}
  collapsed:: true
	- DONE [[Vincent]] on [[AL]] 
	  date:: [[2024-10-21 Mon]]
	- DONE [[Eric]] on [[CL]]
	  date:: [[2024-10-21 Mon]]
	- DONE [[Nick]] on [[AL]] 
	  date:: [[2024-10-15 Tue]]
	  tags:: labor-todo
	  wo:: ANALL
	  time:: 8 hours
	  staffs:: [[Nick]]
	- DONE [[Vincent]] on [[AL]] 
	  date:: [[2024-10-07 Mon]]
	  tags:: labor-todo
	  wo:: ANALL
	  time:: 8 hours
	  staffs:: [[Vincent]]
	- DONE [[Nick]] on `PM` [[CL]] 
	  date:: [[2024-10-07 Mon]]
	  tags:: labor-todo
	  wo:: TECHS
	  time:: 4 hours
	  staffs:: [[Nick]]
	- DONE [[Aaron]] on [[AL]] 
	  date:: [[2024-10-31 Thu]]
- ## [[Maximo]] Labor Data
  id:: 66ff5f43-7dbe-461e-be7b-0d9fb6a86768
  collapsed:: true
	- ### All `Special Labor` records (template name: `special-labor-tp`)
		- DONE Technical Service
		  date:: [[2024-10-09 Wed]]
		  tags:: labor-todo
		  wo:: 651242
		  time:: 0900-1300
		  staffs:: [[Eric]]
		- DONE Technical Service
		  date:: [[2024-10-04 Fri]]
		  tags:: labor-todo
		  wo:: TECHS
		  time:: 4 hours
		  staffs:: [[Vincent]]
		- DONE [[Support of New AMHS for AWOS Messages]]
		  date:: [[2024-10-08 Tue]]
		  tags:: labor-todo
		  wo:: 651523 
		  time:: 0900-1300
		  staffs:: [[All-staffs]]
		- DONE [[Support of New AMHS for AWOS Messages]] 
		  date:: [[2024-10-07 Mon]]
		  tags:: labor-todo
		  wo:: 651523
		  time:: 1400-1800
		  staffs:: [[Aaron]]
	- query-table:: true
	  query-properties:: [:block :date :wo :time :staffs]
	  query-sort-by:: date
	  query-sort-desc:: false
	  collapsed:: true
	  #+BEGIN_QUERY
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
	  :inputs [20241001 20241031 ["Aaron" "All-staffs"]]
	  }
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block :date :wo :time :staffs]
	  query-sort-by:: date
	  query-sort-desc:: false
	  collapsed:: true
	  #+BEGIN_QUERY
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
	  :inputs [20241001 20241031 ["Eric" "All-staffs"]]
	  }
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block :date :wo :time :staffs]
	  query-sort-by:: date
	  query-sort-desc:: false
	  collapsed:: true
	  #+BEGIN_QUERY
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
	  :inputs [20241001 20241031 ["Nick" "All-staffs"]]
	  }
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:block :date :wo :time :staffs]
	  query-sort-by:: date
	  query-sort-desc:: false
	  collapsed:: true
	  #+BEGIN_QUERY
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
	  :inputs [20241001 20241031 ["Vincent" "All-staffs"]]
	  }
	  #+END_QUERY