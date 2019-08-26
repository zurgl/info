## Basic step to install gentoo

### Set up network
```bash
root #ip addr # to get wifiInterface name
root #net-setup wifiInterface
root #ping -c 3 www.gentoo.org # to check network in on
```

### Create a partition's scheme
```bash
$ parted -a optimal /dev/sda
(parted) mklabel gpt
(parted) print # to check  if not empty use rm partNumber
(parted) unti mib
(parted) mkpart primary 1 3
(parted) name 1 grub
(parted) set 1 bios_grub on 
(parted) mkpart primary 3 131
(parted) name 2 boot
(parted) mkpart primary 131 643
(parted) name 3 swap
(parted) mkpart primary 643 -1
(parted) name 4 rootfs
(parted) set 2 boot on
(parted) print
(parted) quit
```

### Choose file system
```bash
root #mkfs.ext2 /dev/sda2
root #mkfs.ext4 /dev/sda4
```

### Activating the swap partition
```bash
root #mkswap /dev/sda3
root #swapon /dev/sda3
```

### Mounting the root partition
```Bash
root #mount /dev/sda4 /mnt/gentoo
```
