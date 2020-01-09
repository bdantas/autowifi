# autowifi
Ditch your bloated network manager

# Purpose
Simple shell script for GNU/Linux that connects to the highest-priority wireless network among the available wireless networks

# What you need
0. GNU/Linux operating system and this script
1. A handful of core and networking utilities (kill, pkill, ifconfig, iwlist, wpa_supplicant, dhclient)
2. Check "user variables" at top of script for correctness
3. Populate the ssid/password combinations as appropriate; if an ssid does not have a password, just use an empty string (note: ssids are searched in order, so list your ssids from highest to lowest priority)

# Installation
```
$ sudo apt install procps net-tools wireless-tools wpasupplicant isc-dhcp-client
$ cd /tmp
$ wget https://github.com/bdantas/autowifi/archive/master.zip
$ unzip master.zip
$ sudo cp ./autowifi/autowifi /usr/local/bin/autowifi
$ sudo chmod a+x /usr/local/bin/autowifi
```
Note: If your operating system is not Debian-like, adjust the first step

# Usage
Run `$ sudo autowifi` at boot or at any other time to connect to the highest-priority wireless network among the currently-available wireless networks.

# Want to see an icon while wifi is connected?
Check out https://github.com/bdantas/wifi-monitor
