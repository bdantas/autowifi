# autowifi
Ditch your bloated network manager

# Purpose
Simple shell script for GNU/Linux that connects to the highest-priority wireless network among the available wireless networks

# Usage
Run `$ sudo autowifi` at boot or at any other time to connect to the highest-priority wireless network among the currently-available wireless networks.

The only adaptations you need to make to the script are:
1. Make sure the wireless interface name at the top of the script is correct for your hardware
2. Populate the ssid/password combinations as appropriate; if an ssid does not have a password, just use an empty string (note: ssids are searched in order, so list your ssids from highest to lowest priority)

# Dependencies
- The utilities the script needs are these: kill, pkill, ifconfig, iwlist, wpa_supplicant, wpa_passphrase, and dhclient
- On **GNU/Linux OS with BusyBox** (e.g., Tiny Core Linux) you probably only have to install three packages: **wireless-tools** (provides iwlist), **wpa_supplicant** (provides wpa_supplicant and wpa_passphrase), and **dhcp** (provides dhclient); BusyBox provides everything else (kill, pkill, ifconfig)
- On **GNU/Linux OS with coreutils** (e.g., Debian) five packages are required: **procps** (provides kill and pkill), **net-tools** (provides ifconfig), **wireless-tools** (provides iwlist), **wpasupplicant** (provides wpa_supplicant and wpa_passphrase) and **isc-dhcp-client** (provides dhclient)

# Want to see an icon while wifi is connected?
Check out https://github.com/bdantas/wifi-monitor
