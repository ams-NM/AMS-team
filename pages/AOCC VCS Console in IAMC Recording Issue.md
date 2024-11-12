tags:: recording, VCS Console,
next-step:: Look for 2 pairs of copper wires from [[IAMC]] to [[ATC]] Equipment room.

- ### Next Steps
	- TODO Use direct copper wires
	- ~~Look for E1-Voice plugins for the MUX~~
	  date:: [[2024-12-01 Sun]]
	  remark:: Need to place wires under floor from console to computer room.
	- ~~==OR== Look for 2 pairs of copper wires from [[IAMC]] to [[ATC]] Equipment room.~~
	  date:: [[2024-12-01 Sun]]
- ## Why
	- [[AOCC]] [[VCS Console]] was located in the room at ATC level 1. Then they asked to move over to [[IAMC]].
	- During the transition, we used a spare [[Console]] port(^^No. 8^^, was `No.12`) in [[VCS]] `Core Switch`.
- ## Ideas
	- ### Option 3: Direct copper wires connections
		- #+BEGIN_NOTE
		  [[DC Team]] found 2 pairs of copper wires. 
		  #+END_NOTE
	- ### ~~Option 2 : Just use the former console port ==No.12==~~
	  collapsed:: true
		- #+BEGIN_NOTE
		  No, it will not work. Need a direct connection from [[VCS Console]] to [[Voice Recorder]] 
		  #+END_NOTE
	- ### ~~Option 1: Find out how to connect new port ==No. 8== to Recording System.~~
	  collapsed:: true
		- There are huge amount of connection wires from [[VCS]] core switch to the nearby [[MDF]].
		- It's really hard to find out where and how they were connected for console recording.
		- #+BEGIN_NOTE
		  Unable to find it.
		  #+END_NOTE
- ## Logs
	- ### [[2024-11-12 Tue]]
		- Morning
			- [[DC Team]] Found a socket near the [[VCS Console]] at [[AOCC]] in [[IAMC]].
			- [[NM]] went and help tested the 2 pairs wire were connected from Console to [[IAMC]]'s computer room.
		- Afternoon
			-
	- ### [[2024-11-06 Wed]]
		- The `Phone` sockets on MUX were verified with telephone sets.
		- Not working.
	- ### [[2024-11-04 Mon]]
		- There is a standalone cable from [[VCS Console]] to recorder
			- 3 cables from Console: 1 to recorder, 2 x 'E1` to [[VCS]] core switch.
			- ![VCS Console connections.png](../assets/VCS_Console_connections_1730778353525_0.png)
			- Ref: [[VCS System Diagram -Built Drawing]]
	- ### [[2024-09-26 Thu]]
		- We haven't found connection of port No.8 to the  `Recording System`.
	-