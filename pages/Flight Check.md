icon:: ✈️

- ## Preparations
  id:: 66ff5f38-b9d4-45b1-9be9-53f47b8b566c
	- TODO Staff arrangement
	- TODO Last records printout
	- TODO Charge battery of portable radio.
	- TODO Any issue need to do during or after?
	- TODO Scan pre-flight check form to PDF & upload to server.
- ## Post Tasks
	- TODO Monitor normalization need?
	- TODO Any measurements of the system for the form?
	- TODO Scan post-flight check form
-
- ## Modifications
  id:: 672042c2-2211-4a07-a55a-9c8f793c3951
	- ### 2024 Oct
	  collapsed:: true
		- ### [[ILS]]
			- ### [[LOC]]
				- Executive Alarm Limits
					- `CRS Width DDM UL`: 17.5% -> 17.7%
					- `CRS Width DDM LL`: 13.4% -> 13.1%
					- `CRS Width DDM UL Pre`: 17.1% -> 17.3%
					- `CRS Width DDM LL Pre`: 13.8% -> 13.5%
				- Tx1 Waveform4: Wide Alarm
					- `CRS SBO Amplitue`: 35.2% -> 35.4%
				- Tx1 Waveform5: Narrow Alarm
					- `CRS SBO Amplitue`: 47.0% -> 47.5%
			- ### [[GP]]
				- Tx2 Waveform1: Operational
					- `CRS CSB1 DDM`: -12.80% -> 12.70%
				- Executive Alarm Limits
					- `CRS Width DDM UL`: 20.1% -> 19.3%
					- `CRS Width DDM LL`: 16.3% -> 16.0%
					- `CRS Width DDM UL Pre`: 19.8% -> 18.8%
					- `CRS Width DDM LL Pre`: 16.5% -> 16.4%
		- ### [[DVOR]] N/A
	- ### 2025 Apr
		- ### [[ILS]]
		  id:: 67fc8ec0-1a2e-42f5-b6dc-6292ab59bc53
			- [[LOC]]
				- [[Monitor Limit]] `Width DDM UL`: 17.3 -> ^^17.1^^; 17.7 -> ^^17.5^^
					- Due to Narrow Alarm not triggered.
			- [[GP]]
				- [[Tx Setting]] `Tx2` `Width`: ^^96%^^
					- [[F.C. Result]]: 0.69 -> ^^0.72^^
					- Monitor reading: 17.2 -> ^^16.4^^
				- [[Tx Setting]] `Tx1` `Width`: ^^98%^^
					- In order to match monitor readings on both Tx, changed setting before hand.
					- [[F.C. Result]]: ^^0.72^^
					- Monitor reading: 17.8 -> ^^17.3^^
				- [[Monitor Limit]] `Width DDM LL`: 16.4 -> ^^15.6^^; 16.0 -> ^^15.2^^
					- Due to Width setting modifications.
			- [[DME]]
				- [[Tx Setting]] ^^[[Reply Delay]]^^: 47.80uA -> ^^49.00uA^^
		- ### [[IGS]]
		  id:: 67fc8ec0-0fb6-492a-859b-37f1f1eefff4
			- [[LOC]]
				- Tx1 `CL DDM`: changed from ^^0.1^^ to ^^0^^
			- [[DME]] (Both Txp): [[How to Change IGS DME Reply Delay]]
				- [[Reply Delay]]: from ^^50.00us^^ to ^^51.00us^^
				- `Beacon Setup` -> `EEPROM` -> ^^Save^^
				- `Beacon Setup` -> `Calibration` -> `Calibrate DELAY` -> Enter ^^51.00us^^
	- ## 2025 Oct
		- ### [[ILS]]
		- ### [[DVOR]]