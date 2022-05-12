## This is my daily notes
### 20220512
I installed gnomes on my ubuntu server today.

1. change into ROOT.

`sudo su root`

2. get the software imformation

`apt-get update`

3. install VNC4Server

`apt-get install vnc4server`

run vncserver

`vncserver`

set password: wjr123

when we see New'VM-32-4-ubuntu:1(root)'desktop is VM-32-4-ubuntu:1, it means the server runs.

4. install X-windows and gdm3 and ubuntu-desktop and gnome packages

`sudo apt-get install x-window-system-core`

`sudo apt-get install gdm3`

`sudo apt-get install ubuntu-desktop`

`sudo apt-get install gnome-panel gnome-settings-daemon metacity nautilus gnome-terminal`

5. modify VNC settings documentation

`vi ~/.vnc/xstartup`

6. restart desktop

`vncserver -kill :1`

`vncserver :1`
