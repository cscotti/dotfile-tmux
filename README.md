# tmux for Linux
Copy `.tmux.conf` to your Home directory

# tmux for wsl/windows

ressource : <https://www.ricalo.com/blog/install-powerline-windows/#install-and-configure-powerline-fonts>

Copy `.tmux.conf_wsl` to your Home directory and rename it to `.tmux.conf`

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

Add this to .zshrc in order to set tmux panes before launch
```
#===================================
# Tmux pan
start_tmux() {
tmux new-session -s "mySession_$(date +%s)" -d
tmux split-window -h
tmux split-window -v
tmux -2 attach-session -d 
}
alias tmux="start_tmux"

```