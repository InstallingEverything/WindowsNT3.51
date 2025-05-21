# **Getting NT 3.51 to install on VMWare Workstation**

Getting Windows NT 3.51 to install on VMWare workstation can be a challenge.

Here is a list of all the things we found in our testing and how we got it working.

1. Creating a new VM and choose Custom install.

![Alt Imgae](Images/VMWare/1a.png)

2. Change the dropdown to Workstation 5.x.

![Alt Imgae](Images/VMWare/2a.png)

3. Select your ISO as normal.

![Alt Imgae](Images/VMWare/3a.png)

4. Select Windows NT from the Windows drop down and carry on.

![Alt Imgae](Images/VMWare/4a.png)

5. Make sure IDE is selected when you get to the HDD section.

![Alt Imgae](Images/VMWare/5a.png)

6. Create a new Virtual Disk

![Alt Imgae](Images/VMWare/6a.png)

7. On this section i tend to chose a disk size of 2tb bigger works but i have run into issues.  Also make sure store in a single file is ticked.

![Alt Imgae](Images/VMWare/7a.png)

8. Finish creating the VM

![Alt Imgae](Images/VMWare/8a.png)

9. Once the machine has created go back into the setting for the VM (DO NOT Start) and choose Advanced under Hard Disk.

![Alt Imgae](Images/VMWare/9a.png)

10. Make sure Disk is set at IDE 0.0.  If it is not you will have issues when installing later Service Packs.

![Alt Imgae](Images/VMWare/10a.png)