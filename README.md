# Table of Contents 
- [Table of Contents](#table-of-contents)
- [Arch install on ASUS ROG Strix](#arch-install-on-asus-rog-strix) 
  - [Basic Installation](#basic-installation)
    - [Boot to the live environment](#boot-to-the-live-environment)
    - [Set keyboard layout](#set-keyboard-layout)
    - [Networking](#networking)
    - [Format disk](#format-disk)


# Arch install on Asus ROG Strix  

**This repo holds my personal guide for installation and configuration of Arch Linux on Asus Rog Strix G15 G513QR. Anyone intending to use this for installation of Arch Linux on their own laptop/notebook are to do it on their own risk.**

**NOTE: This guide is based upon the the installation guide of *[Arch wiki](https://wiki.archlinux.org/title/installation_guide)* and the work of [Unim8arix](https://github.com/Unim8trix/G14Arch), [asus-zephyrus](https://github.com/asus-zephyrus/archinstall) and [Luke Jones](https://asus-linux.org/).**

## Basic Installation

### Boot to the live environment
After acquiring the adequate installation image and preparing an installation medium - a USB flash drive favourably - boot to the live environment. Upon booting you may experiance the first issue, a spam of log messages from nouveau - open-source  driver for NVIDIA graphics cards. You can easily disable/unload the module by using 
```
# modprobe -r nouveau
```
followed by `clear` to remove error message log from your screen. 

NOTE: A standard procedure recommended by *https://wiki.archlinux.org* is to verify the image signature before use. Look up the installation guide for more details.

### Set keyboard layout
The defualt console map of the live environment is set to US. In order to change the setup to appropriate keymap, use 
```
# loadkeys no-latin1
```
(replace 'no' with the shortcut for your country/language). 

### Networking
Start by using command `iwctl` to enter wireless control menu to configure **iwd** daemon. After entering the menu, use the following commands to connect to wifi: 
```
# device list 
# station DEVICE scan 
# station DEVICE get-networks
# station DEVICE connect SSID
```
Exit the menu and control if you are now connected to desired network by typing: 
```
# ping archlinux.org 
```


### Format disk





