#### Install vercel on fish shell

```
curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher
fisher install jorgebucaran/nvm.fish
nvm list-remote
nvm install fermium
nvm use lts/fermium
yarn global add vercel
set -U fish_user_paths /home/zu/.yarn/bin $fish_user_paths
```


Use it

```
vercel
vercel
```
