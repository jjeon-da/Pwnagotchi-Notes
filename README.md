# Pwnagotchi-Notes
collected ramblings to get a pwnagotchi working

## RDNIS Gadget Drivers

Windows RDNIS Gadget Drivers can be found here: https://www.catalog.update.microsoft.com/Search.aspx?q=USB%20RNDIS%20Gadget This was arguably one of the harder things to track down, and is an absolute must-have to connect to raspi through a Windows machine. 

Another surprising linkage was the Bonjour print driver: https://support.apple.com/kb/DL999?locale=en_US while it might just be an element of wizardry, but for whatever reason, this helps,  and i'm not exactly sure why using the 2 together *should work* but I'll sacrifice a few MB of my storage drive to the IT gods so that my code runs.

