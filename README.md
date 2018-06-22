# Snort-Default-Windows-Configuration

### Description ###
By default Snort on Windows comes with Linux paths and relatively bad default configuration. This is a configuration to get Snort 2 (2.9) up and running in no time.

### Instructions ###
1. Install Snort 2:
https://snort.org/downloads
2. Install WinPCap:
https://www.winpcap.org/install/default.htm
3. Download and replace config file from here:
https://github.com/thereisnotime/Snort-Default-Windows-Configuration
4. You can get some nice community rules from here:
https://github.com/thereisnotime/Snort-2-Rules

### Notes ###
Snort on Windows does not like SO rules - that is why they are disabled.
If Snort can't find blacklists, whitelists and other files - an error will be thrown. They need to be presented, even if empty.
Current files that you must create: C:\Snort\rules\black.list and C:\Snort\rules\white.list. If you want to use different files - you must modify the configuration file manually.
Also the configuration presumes that your installation is C:\Snort\, if it is different, then change it manually from the config file.
