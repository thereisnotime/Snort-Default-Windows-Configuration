# Snort-Default-Windows-Configuration

### Description ###
By default Snort on Windows comes with Linux paths, different library names and relatively bad default configuration. This is a configuration to get Snort 2 (2.9) up and running in no time. This guide assumes that Snort is or will be installed in C:\Snort\, if your path is different - please make the necessary adjustment.

### Instructions ###
1. Install Snort 2:

https://snort.org/downloads

2. Install WinPCap:

https://www.winpcap.org/install/default.htm

3. Download and replace config file located in C:\Snore\etc\ path:

https://raw.githubusercontent.com/thereisnotime/Snort-Default-Windows-Configuration/master/snort.conf

4. You can get some nice community rules from here:

https://github.com/thereisnotime/Snort-2-Rules

5. Start your terminal as administrator and type:
```batch
cd C:\Snort\bin
```

6. Determine your interface with:
```batch
snort -W
```

7. Start Snort on 5th (or whatever number yours is) interface:
```batch
snort -i 5 -c C:\Snort\etc\snort.conf
```

### Notes ###
Snort on Windows does not like SO rules - that is why they are disabled.
If Snort can't find blacklists, whitelists and other files - an error will be thrown. They need to be presented, even if empty.
Current files that you must create: C:\Snort\rules\black.list and C:\Snort\rules\white.list. If you want to use different files - you must modify the configuration file manually.
Also the configuration presumes that your installation is C:\Snort\, if it is different, then change it manually from the config file.
