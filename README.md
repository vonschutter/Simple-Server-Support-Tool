# Simple Server Support Tool

![RTD SSST](Media_files/11.png?raw=true "Main Window")


###	Purpose: To simplify support tasks 

	- Display system information 
	- Update system software
	- Bakup virtual machines 
	- Cleanup/Report on PPA's
	- Show systems physical location 
	- Check if a password you intend to use is for sale on the Darknet

You may can run the script on any remote Linux server to manage some common support tasks. This tools should work on any deb or rpm based system or any system that uses package kit to satisfy dependencies and update the system. It uses standard tools available in Lnux and in common repositories tom manage the systems. 

This tools is documentes as well as can be, and it should therefor, also serve as a good learning tool. It It may also easily be extended/modified to do whatever a sys admin would like it to. 
```
Usage: run the script "bash /path/to/rtd" or if installed in the $PATH; by rtd simply type "rtd" in a terminal.
```


![RTD SSST Screenshot 2](Media_files/10.png?raw=true "Executing the Script")

: Validate an intended password to use : 
![RTD SSST Screenshot 2](Media_files/7-pass.png?raw=true "Executing the Script")
: Display results of password vulnerability : 
![RTD SSST Screenshot 2](Media_files/8-pass.png?raw=true "Executing the Script")


We must ensure that the script is run at the proper privileges and in a 
re-attachable session. This means that this script will not allow itself to be run in 
a root terminal or using the sudo command. The reason for this is that, in order to start in
a detachable terminal session "byobu", it may not be launched by root. The script will 
need to be run as a normal administrative user with access to "sudo" a.k.a. a member of the 
"sudoers" security group. This helps adhere to the best practice of NOT using a root interactive
terminal. 

```
NOTE:	This terminal program is written to be readable and documented to a very high degree. The reason is that
	these apps are seldom changed and when they are, it is usefull to be able to understand why and how 
	things were built. Obviously, this becomes a useful learning tool as well; for all people that want to 
	learn how to write admin scripts. It is a good and necessary practice to document extensively and follow
	patterns when building your own apps and config scripts. Failing to do so will result in a costly mess
	for any organization after some years and people turnover. 

	As a general rule, we prefer using functions extensively because this makes it easier to manage the script
	and facilitates several users working on the same scripts over time.
```
