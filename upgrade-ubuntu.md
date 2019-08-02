# Upgrade Ubuntu LTS to Ubuntu 19.04 Using Command Line

Run the following command to upgrade existing software version.

    sudo apt update && sudo apt dist-upgrade

Then make sure you have update-manager-core package installed.

    sudo apt install update-manager-core

Next, edit a configuration file using nano or your preferred command line text editor.

    sudo nano /etc/update-manager/release-upgrades

At the bottom of this file, change the value of Prompt from lts to normal.

    Prompt=normal

Save and exit.

After that, run the following command to begin the upgrade process.

    do-release-upgrade

To check your Ubuntu version, run:

    lsb_release -a