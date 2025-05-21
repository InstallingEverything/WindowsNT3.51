# **Drivers**

We primarly use VMWare here but most of these instructions also work for other product such as VirtualBox.

**Graphics**


**Audio**

Please note this only works on VMWare.

Step 1: Open your vmx file with a text editor, such as notepad, and add this line: sound.virtualDev = "sb16" and save it.

Step 2: Start your guest operating system, it doesn't give you sound right away (9x might be but the chances are small).

Step 3: Open your control panel. For Windows NT 3.51, go to drivers, click add and select the 'creative labs sound blaster 1.X, Pro, 16'. If prompted, insert your Windows installation disc, navigate to D:\i386 (where D is the cdrom drive) and click ok. Leave IQ Adress at 220 and click continue. Now set 'MPU401 IQ address' to disabled. Click OK, Windows wants you to restart, do that. 

You should now have audio.

