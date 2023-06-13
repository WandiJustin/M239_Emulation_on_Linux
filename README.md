# M239_Emulation_on_Linux

A short tutorial to emulate different ROM-Files on Linux Systems with the help of Retro-Emulators. 

# Ubuntu 
To use the following Emulatos you need to setup your Ubuntu Distrobution on a Virtual Machine or a physical machine.

1. Move to [Ubuntu Desktop](https://ubuntu.com/download/desktop "Ubuntu Desktop") and download Ubuntu Desktop (preferrably the newest version).
2. Now install your Ubuntu on your machine ([Virtual Machine](https://www.makeuseof.com/install-ubuntu-on-vmware-workstation/ "Install Ubuntu with VMware Workstation Pro")/[Physical Machine](https://www.dell.com/support/kbdoc/de-ch/000119771/anleitung-zum-erstellen-eines-live-ubuntu-linux-usb-schl%C3%BCssels "Install Ubuntu with Rufus"))

# Dolphine Emulator (Wii/GameCube) 
With Doplhine you can emulate Wii and GameCube games on your system in Full HD. 
[[Source](https://de.dolphin-emu.org/docs/guides/building-dolphin-linux/ "Dolphin-Emu Wiki")]
## Installation
1. To install the stable version input the following commands in the terminal. This will install all necessary packages.
  ```
User@Ubuntu:~$ sudo apt install --no-install-recommends ca-certificates qt6-base-dev qt6-base-private-dev libqt6svg6-dev git cmake make gcc g++ pkg-config libavcodec-dev libavformat-dev libavutil-dev libswscale-dev libxi-dev libxrandr-dev libudev-dev libevdev-dev libsfml-dev libminiupnpc-dev libmbedtls-dev libcurl4-openssl-dev libhidapi-dev libsystemd-dev libbluetooth-dev libasound2-dev libpulse-dev libpugixml-dev libbz2-dev libzstd-dev liblzo2-dev libpng-dev libusb-1.0-0-dev gettext
```
2. Downloade GIT
  ```
User@Ubuntu:~$ sudo apt install git
```
3. Get the Dolphine Repository
  ```
User@Ubuntu:~$ git clone https://github.com/dolphin-emu/dolphin.git dolphin-emu
```
4. Change to the directory created.
  ```
User@Ubuntu:~$ cd ./dolphin-emu
```
5. Pull the GIT submodules
  ```
User@Ubuntu:~/dolphin-emu$ git submodule update --init --recursive
```
6. Create a build subdirectory, and change into it
  ```
User@Ubuntu:~/dolphin-emu$ mkdir Build && cd Build

```
7. Configure the build
  ```
User@Ubuntu:~/dolphin-emu/Build$ cmake ..
```
8. Now run Dolphin
  ```
User@Ubuntu:~/dolphin-emu/Build$ dolphin-emu
```

## ROM Usage

There are a lot of websites to download ROMs from, one we used is [ROMs Games](https://www.romsgames.net/roms/nintendo-wii/ "ROMs Games"). Please be very careful while downloading ROMs, there are a lot of sketchy sites. 

1. Start Dolphin on your machine
2. In the top right corner you can click on "Open"
3. Add your downloaded ROMs to this directory
4. If the ROMs are now not shown in Dolphin restart Dolphin 
