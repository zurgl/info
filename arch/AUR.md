### General 

AUR is Arch User repository Package

### Arch way to install AUR package

```bash
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/paru.git
cd paru 
makepkg -si

```

#### Historically

`yay` is the dedicated tool, but one dev left and do a rust fork.


### Then paru

[paru](https://github.com/Morganamilo/paru)

##### Update system

```bash
paru -Syu # update system 
paru -Sua # only aur package
paru -S icecat # only a package
# or hosrter
paru icecate
paru -Qua # aur package installed that have an update available
paru -R icecate # remove prg
```


### Config file

```
sudo vim paru /etc/paru.conf
```
