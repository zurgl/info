### How to have tab with alacritty


Use tabbed program to solve this issue

```bash
tabbed -r 2 alacritty --embed ""
```

To navigate :
- Ctrl-Shift q to close a tab
- Ctrl-shitf

To know more:
```bash
man alacritty
```


### Add cool font

```bash
yay -S nerd-fonts-fira-code
```

```toml
#.alacritty.yml
# Font configuration (changes require restart)
font:
  normal:
    family: FiraCode Nerd Font Mono
    style: Bold
```


### Cool link
[Gentoo](https://wiki.gentoo.org/wiki/Alacritty)
[Config File example](https://github.com/petobens/dotfiles/blob/master/config/alacritty/alacritty.yml)
