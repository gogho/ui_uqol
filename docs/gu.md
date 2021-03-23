# Games on Ubuntu

Lutris is so far best option for installation. It will install all dependecies in wine with recommended libraries.

[https://linuxconfig.org/install-lutris-on-ubuntu-20-04-focal-fossa-linux](https://linuxconfig.org/install-lutris-on-ubuntu-20-04-focal-fossa-linux)

```bash
sudo apt install libgnutls30:i386 libldap-2.4-2:i386 libgpg-error0:i386 libsqlite3-0:i386
sudo add-apt-repository ppa:lutris-team/lutris
sudo apt-get update
sudo apt-get install lutris 
```

## Hearthstone

[https://lutris.net/games/hearthstone/](https://lutris.net/games/hearthstone/)

### Heartstone with deck tracker

Wine staging is needed. Just create custom wineprefix and start both applications.  
[https://github.com/borisbabic/hearthstone_hdt_linux](https://github.com/borisbabic/hearthstone_hdt_linux)

```bash
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
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine ~/Downloads/Battle.net-Setup.exe 

WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/wine --version
/opt/wine-staging/winecfg
/opt/wine-staging/bin/winecfg 
WINEPREFIX=~/.wine.hearthstone /opt/wine-staging/bin/winecfg 
```


## Diablo 3

[https://lutris.net/games/diablo-iii/](https://lutris.net/games/diablo-iii/)
