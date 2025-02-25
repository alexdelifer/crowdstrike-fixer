# crowdstrike-fixer
An autorun script that fixes the C-00000291*.sys Friday June 19th Crowdstrike crash for systemrescuecd, includes BitLocker mounting support. 

https://www.crowdstrike.com/blog/statement-on-falcon-content-update-for-windows-hosts/

## Instructions: Autorun

Make a "writable filesystem" systemrescuecd usb according to this doc:

 https://www.system-rescue.org/Installing-SystemRescue-on-a-USB-memory-stick/

Copy the `autorun` file from this repo to the /autorun/ folder in the systemrescuecd when mounted from your machine. If the usb is mounted to `/mnt` then the file should be at `/mnt/autorun/autorun`

Boot the usb key on a machine with the following BIOS/UEFI options if applicable
- SATA Operation: AHCI
- Secure Boot: Off

Note: you can set `AHCI` back to `RAID On` after running the script to boot Windows again if needed.

Make sure only 1 Windows HDD or SSD is installed on the machine.

If BitLocker is enabled, dislocker will be run to mount it, have your recovery key handy for this step.

## Instructions: Manually

Just boot a plain old systemrescuecd iso and run the autorun as a shell script

`bash ./autorun`

Same bios settings as above apply.
