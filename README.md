# tmux
Configuration file for tmux

# additional resources if you use wsl with ubuntu and powerline

ressource : <https://www.ricalo.com/blog/install-powerline-windows/#install-and-configure-powerline-fonts>

windows 10/11 session - install powerline required font (with admin role)
```
powershell -command "& { iwr https://github.com/powerline/fonts/archive/master.zip -OutFile ~\fonts.zip }"
Expand-Archive -Path ~\fonts.zip -DestinationPath ~

~\fonts-master\install.ps1
```

ubuntu session - install powerline binary
```
sudo add-apt-repository universe
sudo apt install --yes powerline
```

ubuntu session - To configure Powerline in tmux, add the following to your `~.tmux` file
```
set -g default-terminal "screen-256color"
source "/usr/share/powerline/bindings/tmux/powerline.conf"
```