# PiHole
Network-wide adblocker using Raspberry Pi 3, PiHole, and Netgear R6080 Router
### Setup
* You will need
  * A Raspberry Pi Device (I am using a Raspberry Pi 3)
  * MicroSD card (8GB minimum storage) to install DietPi on
  * A router (I am using the Netgear R6080)
  
* You will need to install 
   * https://www.balena.io/etcher/ to flash DietPi on microSD card
   * https://dietpi.com/ OS we are using to run PiHole
   * https://www.putty.org/ We use Putty to connect to our Raspberry Pi device without needing to physically connect to it

* Run balena etcher and flash the latest DietPi image onto your microSD card.
* Connect microSD card to your Raspberry Pi device, power the device, and connect it to your router using an ethernet cable.
* Look up your Raspberry Pi's IP address by logging into your router through a browser.
* Copy and paste the Raspberry Pi's IP address to Putty and connect.
* Initial login credentials for DietPi are 
  * Username: root
  * Password: dietpi
* Go through the setup process of installing DietPi on your device.
* When finished, copy and paste the following command to install PiHole.
  * curl -sSL https://install.pi-hole.net | bash
* Go through the setup process of installing PiHole on your device.
* Note: Be sure to save the random password PiHole gives you at the end of the installation process for later.
* Reserve your PiHole device's IP address through your router
* Change the range of your router's DHCP range such that your PiHole device IP is not used. 
* Login to your PiHole device by copying/pasting your assigned IP address of it to your browser. 
* Login to PiHole using the random password saved from earlier. 
* Navigate to Group Management > Adlists
* Copy and paste URLs you want blocked from your network. You can find some here: https://firebog.net/
* After adding the links, be sure to update your gravity list. 

### Usage
* For your devices to work with your PiHole device, you must change their DNS settings to use your PiHole's IP address.
