= Customize the look of Debian with desktop-theme-kit =

The package desktop-theme-kit allows admins to customize the look of 
Debian GNU/Linux. In the past, graphics like wallpapers, login 
screens, lock screens or boot menus could be changed at various 
places and sometimes it was still hard to get it to work. Now the 
desktop-theme-kit can do this for you.

At the moment the following applications will use the theme set by 
the desktop-theme-kit: 

Gnome, GDM3, XFCE, KDE, KSplash, KDM, Grub, Grub theme, plymouth, 
slim, lightdm.



== How it works ==

Basically desktop-theme-kit is just pointing all necessary 
configuration files to the pictures you want to use, using Debian 
alternatives whenever possible. 

It also uses its own GUI elements (at the moment for kdm, slim, grub 
theme and plymouth). 



== Who wants to use it ==

desktop-theme-kit is supposed to unify the look of your desktop. It 
does that for ALL users of your system.

So this is an instrument for admins, who want to have the same look 
and feel on all their Debian GNU/Linux systems for all users (for 
instance in a company or a lab). 

This is also a great tool for people who use Debian GNU/Linux as 
their desktop OS and want to see their favorite pictures on more than 
just the desktop wallpaper.



== Who shouldn’t use it ==

People on multiuser systems, who just want to change their wallpaper. 
Not everybody wants to see your cat picture when they log in their 
system. :-)



== Installation ==

Download desktop-theme-kit*.deb and install it by using the command:

dpkg -i desktop-theme-kit.deb

(We are working to get the package into Debian)

Afterwards please run our install script. This script changes the 
lines in various configuration files to point to our theme. Command 
(as root):

update-desktop-theme -i

The script will show you a list of themes that are included in the 
desktop-theme-kit. Please choose one by typing its name. Afterwards 
log out and in (or reboot).



== Using your own pictures ==

desktop-theme-kit comes with six themes included. But you may easily 
create your own: Only three picture files are needed:

*	A login picture (used by GDM3, KDM, Ksplash, slim, lightdm, 
	grub theme and plymouth).

	The picture should be 1920x1080px. 
	If you use KDE, please be aware that KSplash might distort the
	picture. This is a known bug of KSplash. As a workaround use a
	login picture that doesn’t contain circles, swirls or other 
	elements that reveal the distortion. 

	The file should be named “login.png”.

*	A wallpaper (used by Gnome, KDE, XFCE). The preferred size is
	also 1920x1080px. It will be scaled and cropped correctly by all
	three Desktop Environments.
	
	The file should have the name ”wallpaper.png”. 

*	And the classic Grub bootscreen picture. The size should be
	640x480px. The file should be named “grub.png”

At the moment only pictures in PNG format are allowed. Unfortunately 
not all programs accept SVG files.

Now put these three pictures in a folder, give the folder a fitting 
name for instance “forestproject” and copy the folder to:

"/usr/share/images/desktop-themes/*"

As last step, please run 

update-desktop-theme -i  

again. The name of your folder should now be on the list of themes. 
Type it and voilà.



== Uninstall ==

Please use the command:

update-desktop-theme -r

to reset the configuration files to the Debian default theme. Then 
uninstall the package by typing:

dpkg -r desktop-theme-kit

Thanks for using the package. Have fun!



== License ==

desktop-theme-kit

Copyright by Ulrich Hansen <uhansen@mainz-online.de> and 
Ronoaldo JLP <ronoaldo@gmail.com>, 2012, 2013.

It can be used, changed and distributed under the terms of the GNU 
GPL v2 or (at your option) any later version.
