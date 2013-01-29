# Description #

This is for turning my Raspberry Pi into a wireless router.  Not much to it, just trying to make sure I can quickly re-produce "what works".

# Requirements #

## Packages needed/suggested ##
* dnsmasq
* iw
* iptables


## General ##

In my case, I'm using my Raspberry Pi as my WAN-bridge with a switch and Virgin Mobile Mifi device.  My wlan0 will connect to the Mifi (WAN) and eth0 to the switch.  In this case, eth0 is the 'router' port.  I've included configurations for both wlan-router and eth-router.

Some commands to keep in mind:
* sysctl -p
** to make ip forwarding work after config file copy
* route add default gw 192.168.1.1
** this may not be needed after everything is set up and Raspberry Pi rebooted. Might only need it for first time ??  Default route was missing when I tested.


## Reference ##
I used the following to piece together everything I needed.
* http://www.raspberrypi.org/phpBB3/viewtopic.php?f=46&t=25921
* http://sirlagz.net/2012/08/09/how-to-use-the-raspberry-pi-as-a-wireless-access-pointrouter-part-1/
* http://sirlagz.net/2012/08/11/how-to-use-the-raspberry-pi-as-a-wireless-access-pointrouter-part-3/

