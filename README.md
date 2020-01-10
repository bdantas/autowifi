# autowifi
Ditch your bloated network manager

# Purpose
Simple shell script for GNU/Linux that connects to the highest-priority wireless network currently available

# What you need
0. GNU/Linux operating system and this script
1. A handful of non-core utilities: **kill**<sup>1</sup>, **pkill**<sup>1</sup>, **ifconfig**<sup>2</sup>, **iwlist**<sup>3</sup>, **wpa_supplicant**<sup>4</sup>, **wpa_passphrase**<sup>4</sup>, **dhclient**<sup>5</sup>
2. Check "user variables" at top of script for correctness
3. Populate the ssid/password combinations as appropriate; if an ssid does not have a password, just use an empty string (note: ssids are searched in order, so list your ssids from highest to lowest priority)

Debian package names (may be different in other distros):  
1 *procps*  
2 *net-tools*  
3 *wireless-tools*  
4 *wpasupplicant*  
5 *isc-dhcp-client*  

# Installation
```
$ sudo apt install procps net-tools wireless-tools wpasupplicant isc-dhcp-client
$ cd /tmp
$ wget https://github.com/bdantas/autowifi/archive/master.zip
$ unzip master.zip
$ sudo cp ./autowifi-master/autowifi /usr/local/bin/
$ sudo chmod a+x /usr/local/bin/autowifi
```
Note: If your operating system is not Debian-like, adjust the first step

# Usage
Run `sudo autowifi` at boot or at any other time to connect to the highest-priority wireless network among the currently-available wireless networks.

# Want to see an icon while wifi is connected?
Check out https://github.com/bdantas/wifi-monitor
