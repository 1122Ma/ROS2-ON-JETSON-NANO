# ROS2-ON-JETSON-NANO
 Steps for installation ros on jeston nano 
 1-first we can download Xubuntu 
 
 2-after the image is complete , you burn it on the SD card , prepare a program to burn images to an SD card 
 
 3- i use Etcher introduced at https://pinkwink.kr/1189  , launch Etcher and select the Xubuntu image and select the target SD card 
 
 4-when done , remove the SD and connect it to Ubuntu 
 
 5- select the SD card and open it with the file manager , open Boot folder , open extilnux folder , choose toopen terminal from that location 
 
 6- if there are two camera connectors , its B model , Search b00.dtb file , copy file name and then write cd extlinux on terminal , then
 sudo gedit extlinux.conf
 
 7- open extlinux.conf , Type FDT /boot in LABEL primary , and paste dtb file name then  Save and quit 
 
 8-Eject SD card from ubuntu System , insert SD card to jeston nano , Boot in jeston nano , also accept licenses , select language , keyborad layout and set WIFI 
 set location , set user informations , set partition size , finally install and reboot 
 
 9- when its complete , lauunch terminal using CTRL + ALT + T
 sudo apt install net- tools
 check your IP address using command ifconfig 
 
 10- sudo apt install ssh 
 
 launch terminal on my PC  -----> ssh <name of Jeston Nano>@<jeston nano IP>
  
  11- visit gudie page fprinstalling ROS2 Foxy , and follow the set locale process , if you need visit githib.com/jugfk/jeston-fan-ctl
  install dependency 
  git clone 
  
  12-cd jeston-fan-ctl
  sudo sh install.sh
  
  then Fan is activated , follow the setup sources process
  
 13- sudo apt install ros-foxy-desktop
  
  14- test talker node , create new terminal and connect using ssh  then test listene node 
