## What is [NAS](https://en.wikipedia.org/wiki/Network-attached_storage)?
Network-attached storage (NAS) is dedicated file storage that enables multiple users and heterogeneous client devices to retrieve data from centralized disk capacity. Users on a local area network (LAN) access the shared storage via a standard Ethernet connection.

## What is [OMV](https://www.openmediavault.org/)?
openmediavault is the next generation network attached storage (NAS) solution based on Debian Linux. It contains services like SSH, (S)FTP, SMB/CIFS, RSync and many more ready to use. It is a simple and easy to use out-of-the-box solution that will allow everyone to install and administrate a Network Attached Storage without deeper knowledge.

# Let's start the process
## Parts list
![OMV-NAS-Raspberrypi](https://user-images.githubusercontent.com/52346695/210171917-95a3f965-9bf3-42f2-8772-e22add5b4da3.png)
1. [Raspberry pi](https://robu.in/?s=raspberry+pi&product_cat=0&post_type=product) (Recomended raspberry pi 4 with minimum 4GB varient)
2. Micro SD card (Minimum of 16GB class 10)
3. USB 3.0 External HDD/SSD
4. USB SD card reader

## STEP 1: Preaper SD card

```
Warning! Make sure you don't have any data on the SD card.
```
I will use raspberry pi imager to write the image to the sd card. Download it from [raspberrypi.org](https://www.raspberrypi.com/software/). Install it in your computer and plugin the sd card to the same PC. Run the application.
On ```Operating System``` click on the ```CHOOSE OS``` >> ```Raspberry Pi OS (other)``` >> ```Raspberry Pi OS Lite (64-bit)``` then choose your sd card.

IMPORTANT! before writing click on the settings icon bottom. Set host name and enable SSH also set a password

## STEP 2: Setup Raspberry pi
Now put the SD card in raspberry pi and connect network cable and power to the pi

give it some time to boot for the first time.

open a ssh client like [putty](https://www.putty.org/) or open the terminal and try to connect the pi with ssh

```
ssh pi@YOUR_PI_HOST_NAME.local
```
type the password you gave at [STEP 1](https://github.com/souravj96/OMV-NAS-Raspberrypi#step-1-preaper-sd-card)

***If you can't connect to your pi with host name then login to your router and find the IP address of the pi and use that ip instead of HOST_NAME***

first thing first, update the raspberry pi
```
sudo apt update
```
```
sudo apt upgrade -y
```
```
sudo reboot
```
## STEP 3: INSTALL OMV
it's the easiest step of the whole process. just run the bellow command
```
sudo wget -O - https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install | sudo bash
```
for more details open this repository [OpenMediaVault-Plugin-Developers/installScript](https://github.com/OpenMediaVault-Plugin-Developers/installScript)
