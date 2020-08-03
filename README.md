Tilty Pi
========

![](https://cdn.zappy.app/c2f8dd61b5284808531a993217d4e239.png)

A [Raspberry Pi](http://www.raspberrypi.org/) distribution for [Tilt Hydrometers](https://tilthydrometer.com/)

![](https://cdn.zappy.app/859c7a44c7cf2bc04e427b037c5c5372.png)

## Installation ##

Grab a recent [release](https://github.com/myoung34/tilty-dashboard/releases)

  1. Unzip the image and install it to an sd card [like any other Raspberry Pi image](https://www.raspberrypi.org/documentation/installation/installing-images/README.md>)
  1. . Configure your WiFi by editing `tiltypi-wpa-supplicant.txt` on the root of the flashed card when using it like a thumb drive
  1. . Boot the Pi from the card
  1. . Log into your Pi via SSH (it is located the IP address assigned by your router), default username is "pi", default password is "raspberry". Run ``sudo raspi-config``. Once that is open:
   1. Change the password via "Change User Password"
   1. Optionally: Change the configured timezone via "Localization Options" > "Timezone".
   1. Optionally: Change the hostname via "Network Options" > "Hostname".
  
TiltyPi will be located at `http://ipaddress:5000`


## Upgrade ##

To upgrade [tilty](https://github.com/myoung34/tilty) and [tilty-dashboard](https://github.com/myoung34/tilty-dashboard)

  1. SSH into the pi
  1. run `sudo pip3 install -U tilty tilty-dashboard` to upgrade the packages
  1. run `sudo systemctl restart tilty` and `sudo systemctl restart tilty-dashboard` to restart the services
