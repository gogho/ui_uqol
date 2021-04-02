# Raspberry Pi

## Cooler master

```bash
curl https://raw.githubusercontent.com/CoolerMasterTechnology/pi-tool/master/install.sh -o pi-tool-install.sh 
chmod +x pi-tool-install.sh 
./pi-tool-install.sh
```

## SSHF

```bash
sudo apt update
sudo apt install sshfs
mkdir -p ~/.ssh && chmod 700 ~/.ssh
touch ~/.ssh/config
cat > ~/.ssh/config << EOF
Host archibald
	HostName 192.168.1.66
	User gogho
	IdentityFile ~/.ssh/id_rsa
EOF
chmod 600 ~/.ssh/config

ssh-keygen -t rsa -b 4096 -C "gogho1@gmail.com"
ls ~/.ssh/id_*
ssh-copy-id rpi@192.168.1.66
```

### Mount script

```bash
#!/bin/bash
# Ping test for archibald
ping -c 2 archibald > /dev/null
if [ $? -eq 0 ];then
	timeout 1 bash -c 'cat < /dev/null > /dev/tcp/192.168.1.66/22' > /dev/null 2>&1
		if [ $? -eq 0 ];then	
			ssh archibald 'ls /media/gogho/Data/Storage'> /dev/null 2>&1
			if [ $? -eq 0 ];then
				sshfs archibald:/media/gogho/Data/Storage/ /home/pi/archibald/
				echo "Data folder from archibald mounted on /home/pi/archibald"
			else
				echo "Gogho nenamontoval data v archibaldovi"
				exit 1
			fi
		else
			echo "Gogho prepadol temnej strane a je vo windowse"
			exit 1
		fi
else
	echo "Archibald je vypnuty"
	exit 1
fi
```

## Netflix

### Chromium

[https://www.tomshardware.com/how-to/play-netflix-raspberry-pi](https://www.tomshardware.com/how-to/play-netflix-raspberry-pi)  

```bash
curl -fsSL https://pi.vpetkov.net -o ventz-media-pi
sh ventz-media-pi
```

### Netfix via Kodi

[https://pimylifeup.com/raspberry-pi-netflix/](https://pimylifeup.com/raspberry-pi-netflix/)  
[https://howtomediacenter.com/en/install-netflix-kodi-addon/](https://howtomediacenter.com/en/install-netflix-kodi-addon/)  


## VNC setup

[https://www.raspberrypi.org/documentation/remote-access/vnc/](https://www.raspberrypi.org/documentation/remote-access/vnc/)

Already setup, just download [RealVNC](https://www.realvnc.com/en/connect/download/viewer/) and connect

