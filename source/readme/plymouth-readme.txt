- Plymouth - 

If you did run the splashscreen manager plymouth before you installed 
this desktop-theme-*-package, its plymouth theme has now been set 
as your new default. So everything should work. Congratulations!

If you didn't run plymouth before, you probably have to install it.
Plymouth is not automatically installed by Debian.
 
To install it, become root and do:

apt-get install plymouth plymouth-drm

To see a list of available plymouth themes, command:
/usr/sbin/plymouth-set-default-theme --list

and choose your theme:
/usr/sbin/plymouth-set-default-theme theme

To save your changes, run:
update-initramfs -u

To make splashscreens appear at boot, you also have to configure 
the bootmanager Grub. Add "splash" to the line in /etc/default/grub:

GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"

VirtualBox users might want to use the following switch to see the plymouth 
artwork.

GRUB_CMDLINE_LINUX_DEFAULT="quiet splash vga=792"

Finally run
update-grub

See here for additional help in configuring plymouth:
http://wiki.debian.org/plymouth
