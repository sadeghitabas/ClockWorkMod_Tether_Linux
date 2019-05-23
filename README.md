# ClockWorkMod_Tether_Linux

This is an edited version of the CWM tether available source code (Linux: http://download.clockworkmod.com/tether/tether-linux.tgz), owned by ClockworkMod. ClockworkMod Tether is a USB tether solution for Mac, Windows, and Linux that allows you to use your phone's data connection to get internet access on your desktop or laptop.

Need a direct link to the Tether Android installation (APK) file?
http://download.clockworkmod.com/tether/Tether.apk

ClockworkMod Tether does not require root on your phone and does not require a separate tethering plan. Tether should work with any carrier and phone and does not require a carrier's tethering plan. To get around the root requirement on your phone, Tether will need to install a virtual network adapter on your computer; so there is a PC side install.

1) Install this application on your Android phone!

2) Install the Tether software on your PC. If your PC currently has an internet connection, you can download it here:
Mac: http://download.clockworkmod.com/tether/tether-mac.zip
Linux: http://download.clockworkmod.com/tether/tether-linux.tgz
Windows: http://download.clockworkmod.com/tether/TetherWindowsSetup.msi

If your PC does NOT have an internet connection at the moment, start Tether for Android and use the Help button to easily download the PC software to your phone. You can then copy it to your PC and install!

Windows users will also need to install the USB/ADB driver for their phone. Tether's setup process will assist you through that step by step, or you can use the link below!
http://www.clockworkmod.com/tether/drivers

That's it! Connect your phone via USB to your PC, start Tether, and turn it on! Happy surfing!

If you have problems with Tether, please try the following first:
Disable Firewalls and Antivirus software.
Make sure you area not connected to the internet on wireless or ethernet.
Make sure you are using your OEM's USB data cable (and not just a charge cable).

Tether speeds slow?
Your USB speed is limited to the speed of the *slowest* peripheral you have connected. It is recommended you unplug any unnecessary/slow USB peripherals to get maximum Tether speeds.


#### Running Tether on Linux

At the top level directory of the package, run

    sudo linux/run.sh

On the first run of Tether, node.js will be compiled. This will take a few minutes.

#### Compiling for development

    cd node
    make distclean
    ./configure --without-snapshot
    CXXFLAGS=-fpermissive make

#### If you faced with this ERR [Cannot find module 'chainsaw'], follow this:
  You should try using native nodejs and adb installation. Also, make sure your USB debuging is on.
    
    sudo apt install nodejs npm
    sudo apt-get install android-tools-adb android-tools-fastboot
    sudo adb start-server
    sudo apt-get install libncurses5:i386
    sudo adb kill-server
    sudo killall adb
    sudo adb start-server
    npm install chainsaw
    sudo apt-get install net-tools
    sudo linux/run.sh
    
    
  #### If you faced with [Segmentation Fault ERR], YOU CAN USE THE COMPILED VERSION OF THE CODE, you should extract it in your favorate directory and run the [run.sh] file in the Linux folder.
  
  ### Enjoy your Tethering, Good Luck
  ### -ST
