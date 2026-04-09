# Installing Windows NT 3.51 on VMWare Workstation

Getting Windows NT 3.51 to install cleanly on modern VMWare Workstation can be tricky. This guide covers the setup options we tested successfully.

## Requirements

- VMWare Workstation
- Windows NT 3.51 installation ISO
- A new virtual machine configured for older Windows guests

## Step-by-step setup

1. Create a new virtual machine and choose `Custom` install.

![Create a new VM](Images/VMWare/1a.png)

2. Set the virtual hardware compatibility dropdown to `Workstation 5.x`.

![Select Workstation 5.x](Images/VMWare/2a.png)

3. Attach your Windows NT 3.51 ISO as the installation media.

![Select ISO](Images/VMWare/3a.png)

4. Choose `Windows NT` from the Windows guest operating system dropdown and continue.

![Choose Windows NT](Images/VMWare/4a.png)

5. When selecting the hard disk type, make sure `IDE` is selected.

![Select IDE disk](Images/VMWare/5a.png)

6. Create a new virtual disk for the guest.

![Create virtual disk](Images/VMWare/6a.png)

7. For disk size, 2 GB is a reliable choice. Larger disks can work but may cause issues.
   Also ensure `Store virtual disk as a single file` is enabled.

![Disk size settings](Images/VMWare/7a.png)

8. Finish the VM creation wizard.

![Finish setup](Images/VMWare/8a.png)

9. Before starting the VM, open the virtual machine settings and select the hard disk, then choose `Advanced`.

![Open disk advanced settings](Images/VMWare/9a.png)

10. Confirm the disk is set to `IDE 0:0`. If it is not, you may encounter installation or Service Pack update issues later.

![Confirm IDE 0:0](Images/VMWare/10a.png)

## Notes

- A single-file virtual disk is more compatible with older Windows NT builds.
- Use `IDE 0:0` for the primary disk to avoid installer and post-install update problems.
- After these settings are confirmed, the machine should boot into the Windows NT 3.51 installer successfully.
