# <img src="/screenshots/balena-etcher.png" alt="drawing" width="60"/>Etcher-arm-32-64
balena-etcher v1.5.109 and later compiled from [source](https://github.com/balena-io/etcher) for armhf and arm64 for the [Raspberry Pi](https://www.raspberrypi.org) and other [ARM](https://en.wikipedia.org/wiki/ARM_architecture) based [Linux](https://en.wikipedia.org/wiki/Linux) computers.
>NOTE: This only works on Debian and Debian based OS's like Ubuntu.

![Etcher on rpi screenshot](/screenshots/etcher.png)


## Install
It's recommended that you install this version of Etcher from Pi-Apps (click the badge below for more info about pi-apps) <br> 
[![badge](https://github.com/Botspot/pi-apps/blob/master/icons/badge.png?raw=true)](https://github.com/Botspot/pi-apps)  
but if you prefer, you can install it manually: 
1) download the .deb file for your system architecture from the [latest release](https://github.com/Itai-Nelken/Etcher-arm-32-64/releases/latest) (armhf is 32bit arm and arm64 is 64bit arm).
2) open the .deb file with a package installer (just double click it) if you have one installed, or open terminal in the directory where the .deb file is and type 
```bash
sudo apt install -y --fix-broken the-file-name.deb
```
but replace `the-file-name.deb` with the name of the .deb file you downloaded or path to it (E.G. ~/Downloads/balena-etcher-electron_1.5.116+37769efb_armv7l.deb) .
>**explanation:**<br> the `-y` flag tells `apt` to answer yes to all questions,<br> `--fix-broken` tells `apt` to install any needed dependencies.

## compile
Use my [compile script](compile-etcher_v1.5.116.sh), this script simply runs the instructions found [here](https://github.com/futurejones/balena-etcher-arm/blob/master/etcher-build/BUILD.md). To download and run it, simply run the line below in terminal:
```bash
wget -qO- https://raw.githubusercontent.com/Itai-Nelken/Etcher-arm-32-64/main/compile-etcher_v1.5.116.sh | bash
```
Alternatively compile, build and package manually with the instructions [here](https://github.com/futurejones/balena-etcher-arm/blob/master/etcher-build/BUILD.md)
but replace this line: 
```bash
git checkout v1.5.63
```
with this line:
```bash
git checkout v1.5.116
```
so you compile v1.5.116 (newest) instead of v1.5.63.
>**NOTE:**<br>you can put any version you want instead of `1.5.116`, refer to the [table below](https://github.com/Itai-Nelken/Etcher-arm-32-64#recommended-version-numbers-for-the-script).

### use my test script
My test script for now only asks you what version you want to compile and build, in the future it will have a gui using YAD or Dialog.
<br><b>to run:</b><br>download and run the script:
```bash
wget https://raw.githubusercontent.com/Itai-Nelken/Etcher-arm-32-64/main/test-stuff/compile-etcher.sh; bash compile-etcher.sh
```
This command will download and execute my script. The script will be in the directory the Terminal was when running the command.<br>
### recommended version numbers for the script:
version number | notes | compilation armhf/armv7l | compilation arm64/aarch64 |
------------ | ------------- | ------------- | ------------- |
1.5.63 | very old and outdated version but tested and working reliably.<br>not recommended, use only when other versions don't work. | working | not tested,<br>will probably work. |
1.5.116 |  | works | works |
<details>
<summary>Rest of the table above (click to expand)</summary>
<br>
  
| version number | notes | compilation armhf/armv7l | compilation arm64/aarch64 |
| ------------ | ------------- | ------------- | ------------- |
| 1.5.111 | has the newer features. | working | working |
| 1.5.112 | [changelog](https://github.com/balena-io/etcher/blob/master/CHANGELOG.md#v15112). | working | working |
| 1.5.113 | newest version | working | working |
| 1.5.114 |  | works | works |
| 1.5.115 |  | works | works |

</details>

## Uninstall
If you installed from [Pi-Apps](https://github.com/Botspot/pi-apps), then you can also uninstall it from there.If you want to manually uninstall,run the following in terminal:
```bash
$ sudo apt purge balena-etcher-electron
```

## Credits
Big thanks to futurejones for finding a way to compile Etcher for ARM.

- [RaspberryPi Forums thread](https://www.raspberrypi.org/forums/viewtopic.php?f=62&t=255205&start=25).
- [futurejones github repo for balena-etcher-arm](https://github.com/futurejones/balena-etcher-arm)
