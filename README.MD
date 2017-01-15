                                   WinUSB for Ubuntu 16.04

Dependencies : sudo apt-get install gcc build-essential libwxbase3.0-dev libwxgtk3.0-dev

To Compile : 
    git clone https://github.com/sayeed99/WINUSB-Ubuntu-16.04
    cd WINUSB-Ubuntu-16.04
    sudo su
    ./configure
    make
    make install

Fix grub installation : sudo nano /usr/local/bin/winusb
    Find line starting with : grub-install  /line 401 or 402/
    replace this line with : grub-install --target=i386-pc --boot-directory="$partitionMountPath/boot" "$device"

Enjoy!

   Courtesy : https://onetransistor.blogspot.in/2016/04/install-winusb-on-ubuntu-1604-lts.html 
