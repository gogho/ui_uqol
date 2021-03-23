# Ubuntu and windows dualboot setup

## Windows setup for dualboot

### Time differences
[https://ubuntuhandbook.org/index.php/2016/05/time-differences-ubuntu-1604-windows-10/](https://ubuntuhandbook.org/index.php/2016/05/time-differences-ubuntu-1604-windows-10/)

I use local time in ubuntu.

```bash
timedatectl set-local-rtc 1 --adjust-system-clock
#check settting
timedatectl
```
### Disable fastboot

While it was enabled, hard disk could be mounted read-only and motherboard aura was glowing when it was turned off from ubuntu.

1. Go to Control Panel.
2. Click Power Options.
3. Choose "what the power buttons do."
4. Click "Change settings that are currently unavailable."
5. Find and uncheck "Turn on fast startup."
6. Save changes.
7. Shutdown and boot linux.

[https://itsfoss.com/solve-ntfs-mount-problem-ubuntu-windows-8-dual-boot/](https://itsfoss.com/solve-ntfs-mount-problem-ubuntu-windows-8-dual-boot/)

## Ubuntu essencial install

Chrome  

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
cat /etc/apt/sources.list.d/google-chrome.list
```

SMplayer

```bash
sudo add-apt-repository ppa:rvm/smplayer
sudo apt-get update
sudo apt-get install smplayer smtube smplayer-themes
```

Other soft install

```bash
sudo apt install doublecmd-common 
sudo apt install transmission
sudo apt install gnome-tweaks gnome-tweak-tool 
sudo apt install snapd
sudo apt install gparted
sudo apt install net-tools
sudo apt install mlocate
#joplin
wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash
```

Snap installations

```bash
sudo snap install deezer-unofficial-player
sudo snap install docker
# Visual Studio Code
sudo snap install --classic code
```

## Ubuntu configuration

Update grub startup screen to show what is executed

```bash
cat /etc/default/grub
# disable quiet in GRUB_CMDLINE_LINUX_DEFAULT
# GRUB_CMDLINE_LINUX_DEFAULT="splash"
sudo vi /etc/default/grub
sudo update-grub
```

### Startup script to set default audio output to built in audio

From some reason ubuntu always switched default output to USB headset. It is changed after boot to built in audio output.

1. Run: `pactl list short sinks`
2. Note the device name you want to use as default  
alsa_output.usb-Kingston_HyperX_Virtual_Surround_Sound_00000000-00.iec958-stereo	module-alsa-card.c	s16le 2ch 44100Hz	SUSPENDED  
alsa_output.pci-0000_00_1f.3.analog-stereo	module-alsa-card.c	s16le 2ch 48000Hz	SUSPENDED  
3. Try to run: `pactl set-default-sink alsa_output.pci-0000_00_1f.3.analog-stereo`
4. Open the application "Startup Applications" (Should be preinstalled on Ubuntu)
5. Click on "Add", Give your startup item a name 
6. Copy your command from above into the command field and save
`pactl set-default-sink alsa_output.pci-0000_00_1f.3.analog-stereo`

Script can be found in `/home/gogho/.config/autostart/pactl.desktop

## Utils

rsync

```bash
rsync -auvrWz --progress -e ssh gogho@192.168.1.10:/media/gogho/DATA/* .
```

## mkdocs material

Download docker image

```bash
sudo docker pull squidfunk/mkdocs-material  
sudo docker image ls  
```


New project from docker

```bash
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material new .
```

Run local preview

```bash
sudo docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```
