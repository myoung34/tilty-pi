Tilty Pi
========

![](https://cdn.zappy.app/c2f8dd61b5284808531a993217d4e239.png)

A [Raspberry Pi](http://www.raspberrypi.org/) distribution for [Tilt Hydrometers](https://tilthydrometer.com/)

![](https://raw.githubusercontent.com/myoung34/tilty-dashboard/master/images/dash.gif)

## Installation ##

Grab a recent [release](https://github.com/myoung34/tilty-pi/releases)

  1. Unzip the image and install it to an sd card [like any other Raspberry Pi image](https://www.raspberrypi.org/documentation/installation/installing-images/README.md>)
  1. Configure your WiFi by editing `tiltypi-wpa-supplicant.txt` on the root of the flashed card when using it like a thumb drive
  1. (Optional) Configure your configuration by editing [tilty.ini](https://github.com/myoung34/tilty-pi/blob/master/src/modules/tilty/filesystem/boot/tilty.ini)
  1. Boot the Pi from the card. The default ssh username is `pi` and the default password is `raspberry`

**Note** It is recommended to change the ssh password via `raspi-config`.
  
TiltyPi will be located at `http://ipaddress:5000`


## Upgrade ##

To upgrade [tilty](https://github.com/myoung34/tilty) and [tilty-dashboard](https://github.com/myoung34/tilty-dashboard)

  1. SSH into the pi
  1. run `sudo pip3 install -U tilty tilty-dashboard` to upgrade the packages
  1. run `sudo systemctl restart tilty` and `sudo systemctl restart tilty-dashboard` to restart the services
