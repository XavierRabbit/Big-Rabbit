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

##Docker is help to setup enviroment

##install cuda11.5 for ubuntu20.04

link:https://developer.nvidia.com/cuda-11-5-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=20.04&target_type=deb_local

wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin

sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/11.5.0/local_installers/cuda-repo-ubuntu2004-11-5-local_11.5.0-495.29.05-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu2004-11-5-local_11.5.0-495.29.05-1_amd64.deb

sudo apt-key add /var/cuda-repo-ubuntu2004-11-5-local/7fa2af80.pub

sudo apt-get updatesudo apt-get -y install cuda

