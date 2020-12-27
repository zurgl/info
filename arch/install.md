### Get basic stuff

- [Download an iso](https://archlinux.org/download/)
- [Install guide](https://wiki.archlinux.org/index.php/Installation_guide)
- Boot your image


### Set keyboard layout
 ```
localectl set-keymap fr
```


### Set keyboard layout
 ```
timedatectl set-timezone Europe/Paris
```


### Check internet connection
 ```
ping google.com
```


### Partition disk
List and select disk
```
fdisk -l
fdisk /dev/sda
```

Help and gpt partition table creation (label)
```
m
g
```
##### EFI partition
```
n
1
.
+550M
.
```
Partition type
```
t
1
```

##### Swap partition
```
n
2
+2G
.
```
Partition type
```
t
19
```


##### OS partition
```
n
3
.
.

```

##### Write table 
```
w
```


### Formating and mounting partitions
##### For Boot
```
mkfs.fat -F32 /dev/sda1
```

##### For swap
```
mkfs.swap /dev/sda2
swapon /dev/sda2
```

##### For OS
```
mkfs.ext4 /dev/sda3
mount /dev/sda3 /mnt
```

### Installing basic system of arch on OS partition
```
pacstrap /mnt base linux linux-firmware
```

##### Generate filesystem table and chroot
```
genfstab U /mnt >> /mnt/etc/fstab 
arch-chroot /mnt
```

### Basic config before first reboot

##### locale and time set-up
```
ln -sf /usr/share/zoneinfo/Europe/Paris /etc/localtime 
hwclock -systohc
pacman -S nano
nano /etc/locale.gen
locale-gen
```

##### Network stuff
```
nano /etc/hostname
----
switch
----
nano /etc/hosts
----
127.0.0.1 localhost
:::1 localhost
127.0.1.1 switch.localdomaine switch
----
```

##### User

```
passwd
useradd -m zurgl 
passwd zurgl
usermod -aG wheel,audio,video,optical,storage zurgl
pacman -S sudo
EDITOR=nano visudo
## uncomment wheel stuff
```

### Bootloader stuff
```
pacman -S grub efibootmgr dosfstools os-prober mtools
mkdir /boot/EFI
mount /dev/sda1 /boot/EFI
gurb-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
grub-mkconfig -o /boot/grub/grub.cfg
```

### Adding package
```
pacman -S networkmanager vim git
systemctl enable NetworkManager
```

### Reboot
```
umount -l /mnt
reboot # shutdown now for vm to unplug iso
```
