
> bash history
```bash
sudo apt install doublecmd-common 
sudo apt install transmission

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
cat /etc/apt/sources.list.d/google-chrome.list
sudo add-apt-repository ppa:rvm/smplayer
sudo apt-get update
sudo apt-get install smplayer smtube smplayer-themes

cd smplayer/
cp ~/.config/smplayer/smplayer.ini ~/.config/smplayer/smplayer.ini_backup
cp smplayer.ini ~/.config/smplayer/
diff ~/.config/smplayer/smplayer.ini ~/.config/smplayer/smplayer.ini_backup

cat transmission/settings.json
cp transmission/settings.json ~/.config/transmission/

sudo apt-get install gnome-tweaks gnome-tweak-tool 

sudo apt install snapd

sudo apt install gparted

pactl list short sources
cat /etc/pulse/default.pa
sudo vi /etc/pulse/default.pa
pactl list short sinks
pactl list short
pactl list short sinks
pactl set-default-sink alsa_output.pci-0000_00_1f.3.analog-stereo
sudo apt install note
note
wine notepad++


sudo apt install libgnutls30:i386 libldap-2.4-2:i386 libgpg-error0:i386 libsqlite3-0:i386
sudo add-apt-repository ppa:lutris-team/lutris
sudo apt-get update
sudo apt-get install lutris 


sudo snap install deezer-unofficial-player 
deezer-unofficial-player 


sudo apt install tilda 

sudo apt install putty

# set
timedatectl
timedatectl set-local-rtc 1 --adjust-system-clock
timedatectl

cat /etc/default/grub
sudo vi /etc/default/grub
sudo update-grub

rsync
man rsync
rsync -avrW -e ssh gogho@192.168.1.10:/media/gogho/DATA/* .
rsync -avrW --progress -e ssh gogho@192.168.1.10:/media/gogho/DATA/* .
rsync -auvrWz --progress -e ssh gogho@192.168.1.10:/media/gogho/DATA/* .
ssh gogho@192.168.1.10


cat /etc/NetworkManager/conf.d/default-wifi-powersave-on.conf
ifconfig
sudo apt install net-tools 
ifconfig
ping 192.168.1.10
cat /etc/default/grub
ifconfig
sudo apt-get udpate
sudo apt-get update
sudo apt-get upgrade
shutdown now
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo dpkg --add-architecture i386 
sudo apt update
sudo apt list --upgradable
sudo apt upgrade
sudo apt update
sudo apt-get upgrade
reboot
sudo apt-get update
sudo apt-get upgrade
ssh pi@192.168.1.72
exit
su rpi
ssh pi@192.168.1.72
cat /etc/hosts
ifconfig
sudo vi /etc/hosts
ping rpi
mount
ll
cd /media/gogho/Data/
ll
cd /media/gogho/Data/Storage/
ll
su rpi
sudo -i
id
groopus
grooups
grooup
group
groups
sudo usermod -a G gogho rpi
sudo usermod -a -G gogho rpi
mount
cd ..
ll
sudo umount /media/gogho/Data 
shutdown now

WINEPREFIX=~/.wine.hearthstone WINEARCH=win32 wine wineboot
WINEPREFIX=~/.wine.hearthstone winetricks dotnet472
WINEPREFIX=~/.wine.hearthstone winetricks corefonts
WINEPREFIX=~/.wine.hearthstone winetricks nocrashdialog
{ cat | sed 's/$/\r/' | iconv -f ascii -t UTF-16 > /tmp/hdt.reg; } <<EOF
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Wine\X11 Driver]
"UseTakeFocus"="N"

[HKEY_CURRENT_USER\Software\Microsoft\Avalon.Graphics]
"DisableHWAcceleration"=dword:00000001
EOF

WINEPREFIX=~/.wine.hearthstone regedit /tmp/hdt.reg
WINEPREFIX=~/.wine.hearthstone wine ~/Downloads/HDT-Installer.exe
WINEPREFIX=~/.wine.hearthstone winecfg
sudo apt-get li
sudo apt-get install wine-staging
WINEPREFIX=~/.wine.hearthstone winecfg
WINEPREFIX=~/.wine.hearthstone wine ~/Downloads/HDT-Installer.exe
reboot
WINEPREFIX=~/.wine.hearthstone winecfg
WINEPREFIX=~/.wine.hearthstone wine ~/Downloads/HDT-Installer.exe
sudo apt list --installed|grep -i wine
wine --version
whereis wine
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/HDT-Installer.exe
ll ~/.wine.hearthstone/
mv ~/.wine.hearthstone/ ~/wine.hearthstone.old
WINEPREFIX=~/.wine.hearthstone WINEARCH=win32 /opt/wine-staging/bin/wine wineboot
WINEPREFIX=~/.wine.hearthstone winetricks dotnet472
WINEPREFIX=~/.wine.hearthstone winetricks corefonts
WINEPREFIX=~/.wine.hearthstone winetricks nocrashdialog
WINEPREFIX=~/.wine.hearthstone regedit /tmp/hdt.reg
{ cat | sed 's/$/\r/' | iconv -f ascii -t UTF-16 > /tmp/hdt.reg; } <<EOF
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Wine\X11 Driver]
"UseTakeFocus"="N"

[HKEY_CURRENT_USER\Software\Microsoft\Avalon.Graphics]
"DisableHWAcceleration"=dword:00000001
EOF

WINEPREFIX=~/.wine.hearthstone regedit /tmp/hdt.reg
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/HDT-Installer.exe
ls Downloads/|grep -i battle
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/Battle.net-Setup.exe 
INEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/Battle.net-Setup.exe 
cd ~/.wine.hearthstone/drive_c/Program\ Files/
ll
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/HDT-Installer.exe
ifconfig
ps -ef|grep -i hear
kill -9 33675
ps -efH
WINEPREFIX=~/.wine.hearthstone winecfg
winetricks 
wine --version
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine --version
wine=/opt/wine-staging/bin/wine
wine --version
export wine=/opt/wine-staging/bin/winecfg 
wine --version
echo $PATH
whereis wine
ls -la /usr/bin/wine
ls -la /etc/alternatives/
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/winecfg 
shutdown now
ls -altr
du -sh *
rm -rf wine.hearthstone.old/
du -sh .wine
du -sh .wine.hearthstone/
ls -la
ll .wine.hearthstone/drive_c/Program\ Files/Battle.net/
ll Games/hearthstone/
ll Games/hearthstone/drive_c/
du -sh Games/hearthstone/drive_c/*
git
sudo apt install git
/opt/wine-staging/winecfg
/opt/wine-staging/bin/winecfg 
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/winecfg 
winecfg
sudo apt list --installed|grep libvulkan
sudo apt list --installed|grep vulkan
sudo apt install libvulkan1 libvulkan-dev vulkan-utils
cd Downloads/
tar xvf dxvk-1.8.1.tar.gz 
locate visual
sudo apt install mlocate
locate visual
cd ..
ll
mkdir github
cd github/
ll
git config --global user.name "Gogho"
git config --global user.email gogho1@gmail.com
ls -al ~/.ssh
ssh-keygen -t ed25519 -C gogho1@gmail.com
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
sudo apt-get install xclip
xclip -selection clipboard < ~/.ssh/id_ed25519.pub
man git
git clone git@github.com:gogho/ui_uqol.git
ll
cd ui_uqol/
ll
pip
docker
sudo snap install docker
df -h
docker pull squidfunk/mkdocs-material
sudo docker pull squidfunk/mkdocs-material
docker image ls
sudo docker image ls
shutdown now
```