# autowifi
Ditch your bloated network manager

# Purpose
Simple shell script for GNU/Linux that connects to the highest-priority wireless network among the available wireless networks

# Usage
Run `$ sudo autowifi` at boot or at any other time to connect to the highest-priority wireless network among the available wireless networks.

The only adaptations you need to make to the script are:
1. Make sure the wireless interface name at the top of the script is correct
2. Populate the ssid/password combinations as appropriate; if an ssid does not have a password, just use an empty string

# Dependencies
- The utilities the script needs are these: kill, pkill, ifconfig, iwlist, iwconfig, wpa_supplicant, wpa_passphrase and udhcpc
- On **GNU/Linux OS with busybox** you probably only have to install two packages: **wireless-tools** (provides iwlist and iwconfig) and **wpa_supplicant** (provides wpa_supplicant and wpa_passphrase). Busybox provides the other utilities (kill, pkill, ifconfig and udhcpc). 
- On **GNU/Linux OS with coreutils** up to five packages may be required: **procps** (provides kill and pkill), **net-tools** (provides ifconfig), **wireless-tools** (provides iwlist and iwconfig), **wpasupplicant** (provides wpa_supplicant and wpa_passphrase) and **udhcpc**

