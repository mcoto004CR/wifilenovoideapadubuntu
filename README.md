# Enable WiFi in Lenovo Idea Pad Ubuntu

How to enable wifi on a Lenovo IdeaPad using Ubuntu

I recently installed Ubuntu 20 on my Lenovo IdeaPad, to replace Windows.

But I found out that once Ubuntu was ready the Wifi option was not showing on the top right options.

This is due to the fact that the driver is not yet included on this distribution,

To fix it just follow this steps:

    git clone https://github.com/tomaspinho/rtl8821ce.git
    cd rtl8821ce/
    sudo make all

If you found an error that cannot make file, 

  sudo apt-get install build-essential
  
Then 

    sudo make all
    sudo make install
    sudo modprobe -a 8821ce


If you have SecureBoot enabled you will get an error that you dont have permission to modprobe

In this case reboot you laptop , get into Bios (Esc, F2 or Del) during boot disable SecureBoot and when get back in Ubuntu try to modprobe again
  
