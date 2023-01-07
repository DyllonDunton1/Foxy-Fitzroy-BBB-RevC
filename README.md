# Foxy-Fitzroy-BBB-RevC
##Shell Script to set up Foxy Fitzroy and all dependencies on a Beagle Bone Black Rev C. Made to expedite setup for 8 boards that will make a cluster.

#### FIRST STEPS
- Download Ubuntu20.04.5 LTS minimal version for Beagle Bone Black Rev C: https://rcn-ee.com/rootfs/ubuntu-armhf-focal-minimal/2023-01-06/
- Use BalenaEtcher to write the image to an SD card (Preferred >16GB)
- Insert MicroSD Card into BBB and connect board to internet over ethernet
- Connect power cord from BBB to laptop
- run pUTTY and ssh 192.168.7.2 to control the BBB over ssh from the laptop
- default username: ubuntu, default password: temppwd
- reset password using "$ passwd" command

#### SET UP STATIC IP
  `sudo nano /etc/network/interface`
  
  Add in:
  `iface eth0 inet dhcp
   address 192.168.x.xxx
   netmask 255.255.255.0`
   
  SAVE AND REBOOT

#### RUN SETUP

Using putty, connect to that IP address, powering the BBB using power supply rather than laptop
- $ `cd ~`
- $ `git clone https://github.com/DyllonDunton1/Foxy-Fitzroy-BBB-RevC.git`
- $ `./Foxy-Fitzroy-BBB-RevC/foxySetup.sh`
