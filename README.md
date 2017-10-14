# cowfc

This script installs the CoWFC front-end and back-end from https://github.com/mh9924/CoWFC

# BUGS
- After second reboot, the DWC server will start. However the admin GUI to manage consoles, users, bans, etc will not function properly. This has to do with the fact that /var/www/dwc_network/server_emulator/gpcm.db does not have proper permissions set. To fix this, you need to reboot your server after the second reboot. From then onward, everything will function

# TODO
- Automate install for HTML5 Landed template

# NOTES

This script comes in 3 phases. Each phase involves a reboot
-	Add the PHP 7.1 repo
-	Continue CoWFC install
-	Reboot after CoWFC instal
