# Raspberry Pi OS arm64 with XFCE4 from scratch
![](https://github.com/actionschnitzel/pi-os-64-xfce-fs/blob/main/images/main.png?raw=true)



### 1. Get Raspberry Pi OS arm64 Lite and flash it:    
[raspberrypi.com](https://www.raspberrypi.com/software/operating-systems/)
    
### 2. Do the initial setup:
> locale > name/password

### 3. Install dependencies:    
- Update & Upgrade    
``` 
sudo apt update && sudo apt upgrade
```
### 4. Tasksel:
- If not installed:
``` 
sudo apt install tasksel
```
- then:
``` 
sudo tasksel
```
![](https://github.com/actionschnitzel/pi-os-64-xfce-fs/blob/main/images/tasksel_xfce.png?raw=true)

### 5. Login Screen:
``` 
sudo apt install lightdm-settings slick-geeter
```
``` 
sudo reboot
```
### 6. Boot To Desktop:
``` 
sudo raspi-config
```
- 1 System Options > S5 Boot/Auto Login > B3 Desktop
- then exit and reboot    
    
### 7. Config Login:
- Login with Name & Password
- Go to the Start Menu > Settings 
- Scroll down and open the Login Settings
- Configure to you likes
- Go to User TAB and uncheck "Hide User List"

### 7. Install Pi Stuff:
- All the Rasperry Pi custon tools are still missing
``` 
sudo apt install rc-gui rp-bookshelf rp-prefapps
```
- Chromium:
``` 
sudo apt install chromium-browser rpi-chomium-mods
```
- If you need Widevine/DRM for Prime or Disney+:
``` 
sudo apt install chromium-browser:armhf libwidevinecdm0
```
### 8. Dev Stuff:
- The Python env
``` 
sudo apt install python3-dev python3-tk
```
``` 
sudo apt install thonny
```
- Git
``` 
sudo apt install git
```
### 9. Theme Part 1:
[xfce-look.org](https://www.xfce-look.org/browse/)
- to add a theme globaly:
``` 
sudo thunar /usr/share/themes/
```
- copy the theme(s) here    
    
- to add a icons globaly:
``` 
sudo thunar /usr/share/icons/
```
- copy the icons here

### 9. Theme Part 2:
- If you like the default Twister OS Theme:
``` 
sudo apt install numix-gtk-theme numix-icon-theme
```
NOTE: To make a theme really global:    
-Go to: `Setting > Appearance and select a theme` then `Settings > Window Mangers Settings and select a theme`
In XCFE 4.18 it will be no longer nessasary to also change the Window Manager theme
    
- My favorte is The Mint-Y Theme which is in this repo
- Also I use the Papirus Icon Theme + Papirus Folder Mod [Papirus](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme):
``` 
#Icon Theme:
wget -qO- https://git.io/papirus-icon-theme-install | sh

#Folder Theme:
wget -qO- https://git.io/papirus-folders-install | sh

#How To:
#Select the papirus icon theme then:
papirus-folders -C brown --theme Papirus-Dark # replace brown

#Colors:
adwaita,black,bluegrey,breeze,brown,carminecyan,darkcyan,
deeporange,green,grey,indigo,magenta,nordic,orange,palebrown,
paleorange,pink,red,teal,violet,white,yaru,yellow
```
