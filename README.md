# Pwnagotchi-Notes
collected ramblings to get a pwnagotchi working
## RDNIS Gadget Drivers

Windows RDNIS Gadget Drivers can be found here: https://www.catalog.update.microsoft.com/Search.aspx?q=USB%20RNDIS%20Gadget This was arguably one of the harder things to track down, and is an absolute must-have to connect to raspi through a Windows machine. 

Another surprising linkage was the Bonjour print driver: https://support.apple.com/kb/DL999?locale=en_US while it might just be an element of wizardry, but for whatever reason, this helps,  and i'm not exactly sure why using the 2 together *should work* but I'll sacrifice a few MB of my storage drive to the IT gods so that my code runs.

## evilsocket network tethering script
This is one that took a long while to understand.  Going through the manual process of changing the IP, Subnet mask, DNS, etc from within the *Network and Sharing Center* is one way. But those changes seemed to only last for 1 "pluged in" session.  The powershell script sticks the changes, as long as the raspi device is plugged-in, and has booted.  

Use the networking script from the git repo to share internet to the pwnagotchi.

1.	Make sure NetworkManager isn't fucking up your settings. It probably is.

2.	Open powershell as administrator  **you need admin privileges**

3.	set-executionpolicy remotesigned **to allow scripts**

4.	Set-ExecutionPolicy unrestricted **to allow scripts**

5.	https://github.com/evilsocket/pwnagotchi/blob/master/scripts/win_connection_share.ps1

6.	https://github.com/evilsocket/pwnagotchi/blob/master/scripts/macos_connection_share.sh

7.	https://github.com/evilsocket/pwnagotchi/blob/master/scripts/linux_connection_share.sh

8.	Plugin rpi with pwnagotchi sd card inserted.

9.	CD to drive where “*_connection_share.*” is located

10.	“.\win_connection_share -EnableInternetConnectionSharing”

11.	“.\win_connection_share -SetPwnagotchiSubnet”

12.	SSH into the pwnagotchi with default creds. `ssh pi@10.0.0.2` password: raspberry

