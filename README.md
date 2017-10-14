# cowfc

This script installs the CoWFC front-end and back-end from https://github.com/mh9924/CoWFC

# BUGS
- After second reboot, the DWC server will start. However the admin GUI to manage consoles, users, bans, etc will not function properly. This has to do with the fact that /var/www/dwc_network/server_emulator/gpcm.db does not have proper permissions set. To fix this, you need to reboot your server after the second reboot. From then onward, everything will function

# TODO
- Automate install for HTML5 Landed template

# How to use
## Phase 1
Run the following commands:
-	mkdir /var/www
-	cd /var/www
-	chmod +x cowfc.sh
-	./cowfc.sh

The script will update your system. It will then ask you to add the PHP 7.1 repository to APT. Press ENTER

## Phase 2

After reboot, run the following commands:
-	cd /var/www
-	./cowfc.sh

The script will continue the install and reboot your server when done

## Phase 3

This last phase fixes a bug whe gpcm.db does not have proper file permissions.

Let the server boot up, and wait a minute or so and issue:
-	reboot

This will reboot the server and set proper permissions
# NOTES

This script comes in 3 phases. Each phase involves a reboot
-	Add the PHP 7.1 repo
-	Continue CoWFC install
-	Reboot after CoWFC instal
