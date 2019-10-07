# autowifi
Ditch your bloated network manager

# Purpose
Simple shell script for GNU/Linux that connects to the highest-priority wireless network among the available wireless networks

# Usage
Run `$ sudo autowifi` at boot to connect to highest-priority wireless network among the available available wireless networks. If later you come within range of a higher-priority network and want to switch to it, just run `$ sudo autowifi` again.

# Dependencies
- The utilities the scripts needs are: kill, pkill, ifconfig, iwlist, iwconfig, wpa_supplicant, wpa_passphrase and udhcpc
- On **GNU/Linux OS with busybox** - You probably only have to install two packages: **wireless-tools** (provides iwlist and iwconfig) and **wpa_supplicant** (provides wpa_supplicant and wpa_passphrase). Busybox provides the other utilities (kill, pkill, ifconfig and udhcpc). 
- On **GNU/Linux OS with coreutils** - Up to five packages may be required: **procps** (provides kill and pkill), **net-tools** (provides ifconfig), **wireless-tools** (provides iwlist and iwconfig), **wpasupplicant** (provides wpa_supplicant and wpa_passphrase) and **udhcpc**

