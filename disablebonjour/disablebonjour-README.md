#READ ME FOR DISABLE BONJOUR SCRIPT
===========

By default Macs advertise their existence on the network they are connected to with a DNS Multicast protocol.  This allows one Mac to see and easily connect to other Macs and devices on the network.  This doesn't work so well when you have hundreds of Macs on the same network and businesses, schools, and data centers regularly disable this functionality.  It can be done by edited a plist file and adding in a specific flag.  If this file is not edited properly, the Mac can cease to resolve DNS or may no longer boot.  This script quickly detects the version of OS X and makes sure the flag is not currently sets and painlessly edits the plist file.

This script was developed and tested by the staff of Mac Mini Vault, we colocate a lot of Macs and tirelessly work to add usability and streamline the plight of the Mac in the data center world.  Check out our website at http://www.macminivault.com

#WHAT THIS SCRIPT DOES
+ Checks to make sure OS X is at 10.6.x or newer
+ Checks to make sure 'NoMulticastAdvertisements' flag isn't already present (10.6-10.9)
+ Adds 'NoMulticastAdvertisements' flag to the proper plist file (10.6-10.9)
+ Checks to make sure '--no-multicast' flag isn’t already present (10.10.0 to 10.10.3)
+ Adds '--no-multicast' flag to the proper plist file (10.10.0 to 10.10.3)

#INSTALLATION

+ Open Terminal and run the following command

        bash <(curl -Ls http://git.io/q9j5Zw)
:exclamation: [**Security Notice**](https://github.com/MacMiniVault/Mac-Scripts#readme)

+ Enter in your password when prompted.
+ Reboot after script completion.
