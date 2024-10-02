# MagicMirror-splashscreen
Add splash screen for MagicMirror

## Installation
Install required modules
```shell
sudo apt install plymouth-themes
```

Make dir for theme
```shell
sudo mkdir /usr/share/plymouth/themes/MagicMirror
```

**Copy files to folders**
```shell
cd ~
git clone https://github.com/erdemarslan/MagicMirror-splashscreen.git

sudo mkdir ~/MagicMirror/splashscreen

sudo cp ~/MagicMirror-splashscreen/MagicMirror.plymouth ~/MagicMirror/splashscreen/MagicMirror.plymouth

sudo cp ~/MagicMirror-splashscreen/MagicMirror.script ~/MagicMirror/splashscreen/MagicMirror.script
```
Use code below if you used vertical layout of screen.
```shell
sudo cp ~/MagicMirror-splashscreen/splash.png ~/MagicMirror/splashscreen/splash.png

sudo cp ~/MagicMirror-splashscreen/splash_halt.png ~/MagicMirror/splashscreen/splash_halt.png
```
Use code below if you used horizontal (right rotated) layout of screen.
```shell
sudo cp ~/MagicMirror-splashscreen/splash_right.png ~/MagicMirror/splashscreen/splash.png

sudo cp ~/MagicMirror-splashscreen/splash_halt_right.png ~/MagicMirror/splashscreen/splash_halt.png
```

Now we can set theme:
```shell
sudo cp ~/MagicMirror/splashscreen/splash.png /usr/share/plymouth/themes/MagicMirror/splash.png && sudo cp ~/MagicMirror/splashscreen/MagicMirror.plymouth /usr/share/plymouth/themes/MagicMirror/MagicMirror.plymouth && sudo cp ~/MagicMirror/splashscreen/MagicMirror.script /usr/share/plymouth/themes/MagicMirror/MagicMirror.script

sudo plymouth-set-default-theme -R MagicMirror
```
Reboot the system
```shell
sudo reboot
```
