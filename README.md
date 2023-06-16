# M239_Emulation_on_Linux
###### By Justin Wandeler & Joel Sassi

A short tutorial to emulate different ROM-Files on Linux Systems with the help of Retro-Emulators. 

# Ubuntu 
To use the following Emulators you need to set up your Ubuntu Distribution on a virtual machine or a physical machine.

1. Move to [Ubuntu Desktop](https://ubuntu.com/download/desktop "Ubuntu Desktop") and download Ubuntu Desktop (preferably  the newest version).
2. Now install your Ubuntu on your machine ([Virtual Machine](https://www.makeuseof.com/install-ubuntu-on-vmware-workstation/ "Install Ubuntu with VMware Workstation Pro")/[Physical Machine](https://www.dell.com/support/kbdoc/de-ch/000119771/anleitung-zum-erstellen-eines-live-ubuntu-linux-usb-schl%C3%BCssels "Install Ubuntu with Rufus")).

![Dolphin Ubuntu](https://cdn2.steamgriddb.com/file/sgdb-cdn/logo/860ec4b483f4eb74c18dff91f162331a.png "Dolphin")
# Dolphin Emulator (Wii/GameCube)
With Doplhin you can emulate Wii and GameCube games on your system in Full HD. 
[[Source](https://de.dolphin-emu.org/docs/guides/building-dolphin-linux/ "Dolphin-Emu Wiki")]
## Installation
1. Install all packages and also the stable version
  ```
User@Ubuntu:~$ sudo apt install --no-install-recommends ca-certificates qt6-base-dev qt6-base-private-dev libqt6svg6-dev git cmake make gcc g++ pkg-config libavcodec-dev libavformat-dev libavutil-dev libswscale-dev libxi-dev libxrandr-dev libudev-dev libevdev-dev libsfml-dev libminiupnpc-dev libmbedtls-dev libcurl4-openssl-dev libhidapi-dev libsystemd-dev libbluetooth-dev libasound2-dev libpulse-dev libpugixml-dev libbz2-dev libzstd-dev liblzo2-dev libpng-dev libusb-1.0-0-dev gettext
```
2. Download GIT
  ```
User@Ubuntu:~$ sudo apt install git
```
3. Get the Dolphin Repository
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

8. From here build and install in the standard make way

  ```
User@Ubuntu:~/dolphin-emu/Build$ make -j$(nproc)

User@Ubuntu:~/dolphin-emu/Build$ sudo make install
```

9. Now run Dolphin
  ```
User@Ubuntu:~/dolphin-emu/Build$ dolphin-emu
```

### ROM Usage in Doplhin

There are a lot of websites to download ROMs from, the one we used is [ROMs Games](https://www.romsgames.net/roms/nintendo-wii/ "ROMs Games"). Please be very careful while downloading ROMs, there are a lot of sketchy sites. 

1. Start Dolphin on your machine
2. In the top right corner you can click on "Open"
3. Add your downloaded ROMs to this directory
4. If the ROMs are now not shown in Dolphin restart Dolphin
   
![Dolphin on Ubuntu](https://i.imgur.com/0rDtUTJ.png "Dolphin EMU on Ubuntu")

# VisualBoyAdvance on Ubuntu (GBA/GBC/GB) 
![VBA](https://i0.wp.com/visualboyadvance.org/wp-content/uploads/2022/08/cropped-visual-boy-advance-logo.webp?w=512&ssl=1 "VBA")

With VisualBoyAdvance (VBA) you can play GameBoy, GameBoy Color and Gameboy Advanced ROMs on almost any operating system. [[Source](https://visualboyadvance.org/install-linux/ "VBA Site")]
## Installation 
Follow the instructions to install and start VBA. 
1. Update your OS
  ```
User@Ubuntu:~$ sudo apt-get update
```
2. Upgrade installed files
  ```
User@Ubuntu:~$ sudo apt-get upgrade -y 
```
3. Install VisualBoyAdvance
  ```
User@Ubuntu:~$ sudo snap install visualboyadvance-m --beta
```
## Running VBA
### Run VisualBoyAdvance through the terminal
  ```
User@Ubuntu:~$ visualboyadvance-m
```

### You can also run VBA through the application explorer 
1. Go to "show applications"
2. Type in
  ```
VBA-M
```
3. Click on it!

![VBA Installed ](https://i0.wp.com/visualboyadvance.org/wp-content/uploads/2022/11/show-vba-m-app.png?w=373&ssl=1 "VBA Installed")

### ROM Usage in VBA
You can get your ROM's as an example from [ROMs Games](https://www.romsgames.net/roms/ "ROMs Games"). Please be very careful while downloading ROMs, there are a lot of sketchy sites.
1. After you started VBA you're presented with a black screen
2. To open a GBA ROM go to *File > Open...* or press *CTRL + O*
3. For GB or GBC ROMs go to *File > Open GB*... or *File > Open GBC...*
![VBA Open ROM ](https://i0.wp.com/visualboyadvance.org/wp-content/uploads/2022/11/visual-boy-advance-installed-on-linux.jpg?w=794&ssl=1 "VBA Open ROM")

# ZSNES on Linux (NES/SNES) 
With ZSNES you can emulate NES and SNES ROMs. [[Source](https://www.debugpoint.com/3-nes-emulators-to-play-old-nes-games-in-linux/ "ZSNES Tutorial")] [[Source](https://wiki.ubuntuusers.de/ZSNES/
 "ZSNES Tutorial")]
 
## Installation 
Follow the instructions to install and start VBA. 
1. Update your OS
  ```
User@Ubuntu:~$ sudo apt-get update
```
2. Upgrade installed files
  ```
User@Ubuntu:~$ sudo apt-get upgrade -y 
```
3. Install zsnes
  ```
User@Ubuntu:~$ sudo apt install zsnes
```
![ZSNES Installation](https://www.debugpoint.com/wp-content/uploads/2016/07/ZSNES-Main.png "SNES Installation")

## Running ZSNES
You can run ZSNES through the application explorer 
1. Go to "show applications"
2. Type in
  ```
ZSNES
```
3. Click on it!

### ROM Usage in ZSNES
You can get your ROM's as an example from [ROMs Games](https://www.romsgames.net/roms/ "ROMs Games"). Please be very careful while downloading ROMs, there are a lot of sketchy sites.
1. After you started ZSNES you're presented with a start up screen
2. To open a NES or SNES ROM you go to *Game > Load* and select your ROM. 
![VBA Open ROM ](https://i0.wp.com/visualboyadvance.org/wp-content/uploads/2022/11/visual-boy-advance-installed-on-linux.jpg?w=794&ssl=1 "VBA Open ROM")

# RetroArch on Linux
With RetroArch enables you too emulate a whole lot of consoles. As an example: Dolphin is already incluced in RetroArch, and many more. [[Source](https://www.retroarch.com/index.php?page=linux-instructions "RetroArch Tutorial")] 

## Installation 
Follow the instructions to install and start VBA. 
1. Update your OS
  ```
User@Ubuntu:~$ sudo apt-get update
```
2. Upgrade installed files
  ```
User@Ubuntu:~$ sudo apt-get upgrade -y 
```
3. Install RetroArch
  ```
User@Ubuntu:~$ sudo add-apt-repository ppa:libretro/stable && sudo apt-get update && sudo apt-get install retroarch
```
![RetroArch](https://www.addictivetips.com/app/uploads/2019/03/retroarch1-e1552001701690.jpg "SNES Installation")

## Running RetroArch
You can run RetroArch through the application explorer 
1. Go to "show applications"
2. Type in
  ```
RetroArch
```
3. Click on it!
