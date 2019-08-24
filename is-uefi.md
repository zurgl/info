## How to know if your pc is uefi and what's uefi

### What's uefi mean ?

uefi is the succesor of bios it's a low-level hard-software dedicated to manage 
hardware detection and boot, phase which happen before os-booting phase.

This new standard allow some improvement targetin disk-storage and CPU.

### How to know if my pc support uefi ?

Look up for */sys/firmware/efi* folder's, if you'll find it then uefi is yours 
else you've bios.

### Tips 

On debian-based system install efibootmgr to manage uefi.
