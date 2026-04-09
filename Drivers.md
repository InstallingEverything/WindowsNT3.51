# Windows NT 3.51 Drivers

This page collects driver guidance for Windows NT 3.51, with a focus on VMWare and other virtual machine environments.

## Contents

- [Graphics](#graphics)
- [Audio](#audio)

## Graphics

Driver support for graphics adapters is still being collected. If you have working configurations for VMWare or VirtualBox, add them here.

## Audio

These instructions are tested with VMWare Workstation and enable Sound Blaster compatibility for Windows NT 3.51.

### VMWare setup

1. Shut down the VM.
2. Open the VM's `.vmx` file in a text editor.
3. Add or update the following line:

   ```
   sound.virtualDev = "sb16"
   ```

4. Save the file and restart the VM.

### Windows NT 3.51 driver installation

1. Open Control Panel in the guest.
2. Go to `Drivers`, then click `Add`.
3. Choose `Creative Labs Sound Blaster 1.X, Pro, 16`.
4. If prompted, insert the Windows NT 3.51 installation disc and browse to `D:\i386` (replace `D:` with the guest CD-ROM drive letter).
5. Leave `IRQ Address` at `220` and continue.
6. Set `MPU401 IRQ Address` to `Disabled`.
7. Click `OK` and allow Windows to restart.

After reboot, audio should be available in the NT 3.51 guest.

## Notes

- These audio steps are known to work in VMWare; VirtualBox support may require a different virtual sound device.
- If audio does not appear after reboot, verify the `.vmx` file entry and the selected Sound Blaster driver in NT.

