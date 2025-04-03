icon:: 👨‍⚕️

- ## Current issues
- ### [[ILS]]
	- GP ==CRS Width DDM== [Tx-1: 17.1; Tx-2: 18.6]
	- GP & DVOR DME output power issues
		- [[🐞CM -GP DME Output power is too low]]
	- GP DME Tx2 shutdown
	  collapsed:: true
		- CM: 364094, 471713
		- ```
		  On 28-Apr-2017, 03:00LT replaced TFS#2, MIN#2, TRC#2 and TPR#2 for shutdown fault diagnostic issue.
		  Checked DME history, TX#2 normal, no shut down issue found till to 30-Jul-2017
		  
		  On 04-Aug-2017, sent defective module for repair as below:-
		  1. Monitor Interrogator (MIN) #2451108, S# 12B410005 PCS06 ----- Received on 04-Jul-2018 (No Repair Report)
		  2. Receiver (TRC) #474910037Z, S# 08B300008 PCS02  ------- Received on 04-Jul-2018 (No Repair Report) 
		  3. Processor (TPR) #4451219, S# 12B050002 PCS03    ----- Received new TPR #4452129, S#14B270008PCS03 on 04-Jul-2018
		  4. Frequency Synthesizer (TFS) #2451111, S# 08B300012 PCS07 ---- Received on 30-Jan-2018 (Thales Fault Report: Module Faulty, replaced TR401 broken component)
		  ```
- ### [[DVOR]]
	- DVOR output power inconsistence & too high lately:
	  | Date | Tx1 -Mon 1 | Tx1 -Mon 2 | Tx2 -Mon 1 | Tx2 -Mon 2 |
	  | ---| ---| ---| ---| --- |
	  | 2021-11 | 1176w | 924w| 1175w | 1005w |
	  | 2023-01 | 833w| 811w| 912w | 892w |
	  | 2023-03 | 991w | 900w | 1232w | 962w |
		- ![image.png](../assets/image_1684134729736_0.png)
- ### [[IGS]]
	- IGS DME Output Power Difference Larger Than 10w
		- Ref: TS 608628
- ## Followup
- ## Logs
- Pre-meeting in CAM North Extension Level-3 meeting room. -[[2023-01-16 Mon]]