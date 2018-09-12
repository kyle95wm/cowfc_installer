# cowfc

This script installs the CoWFC front-end and back-end from https://github.com/mh9924/CoWFC

# CONTRIBUTING

Please open pull requests for the dev branch.

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

# NOTES

This script comes in 3 phases. Each phase involves a reboot
-	Add the PHP 7.1 repo
-	Continue CoWFC install
-	Reboot after CoWFC instal
