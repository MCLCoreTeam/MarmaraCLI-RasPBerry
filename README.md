# Raspberry Pi Desktop - Debian - (Komodo) Portable Kurulumu


**Aciklama** Raspberry Komodo kurulumu için dosyaları çektikten sonra yapmanız gerekenler.

Gereksinimler
```
https://www.raspberrypi.org/downloads/raspberry-pi-desktop/
Debian Stretch with Raspberry Pi Desktop
The Raspberry Pi Desktop OS for PC and Mac - based on Debian Stretch
Version:April 2019
Release date:2019-04-11
Kernel version:4.9
```

Uyumlu sürümler (Supported Raspberry Pi)
```
Raspbian Stretch with desktop and recommended software
Raspbian Stretch with desktop
Raspbian Stretch Lite
NOOBS (Offline and network install)
NOOBS Lite (Network install only)
Install Ubuntu Server on a Raspberry Pi 2 or 3
```

Uyumlu Cihazlar
```
Rasp
Raspberry Pi 2 Model B
Raspberry Pi 3 Model B
Raspberry Pi 3 Model B+ (recommended)
Raspberry Pi 3 Model A+ (not recommended)
Raspberry Pi 1 Model A+
Raspberry Pi 1 Model B+
Raspberry Pi Zero
Raspberry Pi Zero W
```

-----------------------------------------------------------------------------------------------------
Part 1
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install libcurl3-gnutls:amd64
sudo apt-get install libcurl4-openssl-dev:amd64
sudo apt-get install libcurl3
```

Part 2
```
sudo apt-get update
sudo apt-get upgrade -y
sudo apt install ufw
sudo ufw --version
sudo ufw enable
sudo apt-get install ssh
sudo ufw allow "OpenSSH"
sudo ufw allow 56141
sudo apt-get install build-essential pkg-config libc6-dev m4 g++-multilib autoconf libtool ncurses-dev unzip git python zlib1g-dev wget bsdmainutils automake libboost-all-dev libssl-dev libprotobuf-dev protobuf-compiler libgtest-dev libqt4-dev libqrencode-dev libdb++-dev ntp ntpdate software-properties-common curl clang libcurl4-gnutls-dev cmake clang -y
sudo apt-get install libsodium-dev
```

Part 3
```	
cd /tmp
wget https://github.com/nanomsg/nanomsg/archive/1.0.0.tar.gz -O nanomsg-1.0.0.tar.gz --no-check-certificate
tar -xzvf nanomsg-1.0.0.tar.gz
cd nanomsg-1.0.0
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/usr
cmake — build .
sudo ldconfig
```	

Part 3.1
```
git clone https://github.com/nanomsg/nanomsg
cd nanomsg
cmake .
make
sudo make install
sudo ldconfig
```
  
Part 4
```
cd ~
wget https://github.com/narGoThic/Raspberry-Marmara/releases/download/RaspberryKOMODO/MarmaraCLI.tar.gz
tar -xvf MarmaraCLI.tar.gz
mkdir .zcash-params
mv ~/MarmaraCLI/.zcash-params/* ~/.zcash-params
```

Kullanım 

```
cd ~/MarmaraCLI
./marmarad -ac_name=MTST3 $1 $2 $3 $4  // Start
./marmara -ac_name=MTST3 $1 $2 $3 $4 // Komutlar
```



İletişim (Contact) B. Gültekin Çetiner http://twitter.com/drcetiner & ~Paro, (c) 2019
