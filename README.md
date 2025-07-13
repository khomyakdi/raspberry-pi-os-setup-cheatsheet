# My Raspberry PI cheat sheet

## connect wifi

```
nmcli radio wifi on
nmcli device wifi list
nmcli device wifi connect "SSID" password "PASSWORD"
```

## i3

### Install

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install i3 xserver-xorg xinit
startx
```

### Setup

```
sudo apt install rofi polybar alacritty

mkdir ~/.config/polybar
touch ~/.config/polybar/config.ini
touch ~/.config/polybar/launch.sh
chmod +x ~/.config/polybar/launch.sh
```


Code for i3 config (`~/.config/i3/config`)
```
bindsym $mod+Return exec urxvt
bindsym $mod+q kill
bindsym $mod+d exec --no-startup-id rofi -show drun
bindsym $mod+Shift+d exec --no-startup-id rofi -show filebrowser
exec_always --no-startup-id ~/.config/polybar/launch.sh &
```

## Packages

- `chromium` - Chromium
- `dolphin` - File manager
- `lxappearance` - appearance setup