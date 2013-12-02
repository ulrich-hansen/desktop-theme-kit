![headline](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/headline.png) 

In the past, graphics like wallpapers, login screens, lock screens or boot menus had to be configured in various places. And sometimes it was still hard to get it to work. 

Now the desktop-theme-kit can do this for you.


## One look

Once installed, the whole system will share the same look. The grub menu, the bootscreen, the desktop and more. At the moment, desktop-theme-kit provides artwork for the following applications: 

| **Grub2** | **Grub2 Theme** | **Plymouth** |
|:--------:|:--------:|:--------:|
|[![roj-grubclassic](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-grubclassic-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-grubclassic.png)|[![roj-grubtheme](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-grubtheme-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-grubtheme.png)|[![roj-plymouth](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-plymouth-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-plymouth.png)|
| **GDM3** | **Gnome** | **KDM** |
|[![roj-gdm3](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-gdm3-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-gdm3.png)|[![roj-gnome](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-gnome.png)|[![roj-kdm](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-kdm-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-kdm.png)|
| **KSplash** | **KDE** | **slim** |
|[![roj-ksplash](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-ksplash-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-ksplash.png)|[![roj-kde](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-kde-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-kde.png)|[![roj-slim](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-slim-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-slim.png)|
| **lightdm** | **LXDE** | |
|[![roj-lightdm](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-lightdm-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-lightdm.png)|[![roj-lxde](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-lxde-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-lxde.png)||


## Six themes included - and easily add your own!

desktop-theme-kit comes with six themes:

| **Roj** | **Growing** | **Elegance Blue** |
|:--------:|:--------:|:--------:|
|[![Roj](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/roj-wallpaper.png) | [![Growing](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/growing-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/growing-wallpaper.png)|[![Elegance Blue](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/elegance-blue-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/elegance-blue-wallpaper.png)|
| **Elegance Sepia** | **Jethro** | **Journey** |
|[![Elegance Sepia](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/elegance-sepia-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/elegance-sepia-wallpaper.png) | [![Jethro](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/jethro-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/jethro-wallpaper.png)|[![Journey](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/journey-gnome-preview.png)](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/journey-wallpaper.png)|

And you can easily create your own themes! Just look up [installation](#installation) a bit further.

 
## Our users

desktop-theme-kit is supposed to unify the look of your desktop. It does that for **ALL** users of your system. 

* So this is an instrument for admins, who want to have the same look and feel on all their Debian GNU/Linux systems for all users (for instance in a company or a lab).  

* This is also a great tool for people who use Debian GNU/Linux as their desktop OS and want to see their favorite pictures on more than just the desktop wallpaper. 

## Who shouldn't use it 

People on multiuser systems, who just want to change their wallpaper. Not everybody wants to see your star wars pictures when they log in their system. :-) 

 

## [Installation](id:Installation)

At the moment, desktop-theme-kit is supposed to be installed in two steps:

1. The .deb-package lays the groundwork. It installs all the files needed, updates Debian alternatives, sets symbolic links and puts configuration files in place.

2. The install script "update-desktop-theme" lets you select a theme. It points all necessary configuration files to the pictures you want to use, using Debian alternatives whenever possible.

Download [desktop-theme-kit*.deb] (downloads) and install it by using the command: 

`dpkg -i desktop-theme-kit*.deb`

Afterwards please run the install script. Command (as root): 

`update-desktop-theme -i`

The script will show you a list of themes that are included in the desktop-theme-kit. Please choose one by typing its name. 

![install1](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/update-desktop-theme-1a.png)

The script will now activate the chosen theme. When it is done, please log out and in (or reboot). 


### Use your own pictures

You may easily add your own themes. Only three pictures are needed: 

* A login picture (used by GDM3, KDM, Ksplash, slim, lightdm, 	grub theme and plymouth). The picture should be **1920x1080px**. 	The file should be named **login.png**. 

* A wallpaper (used by Gnome, KDE, XFCE). The preferred size is also **1920x1080px**. Please name the file **wallpaper.png**.  

* And the classic Grub bootscreen picture. The size should be **640x480px**. The file should be named **grub.png** 

At the moment only pictures in **PNG** format are allowed. 

Now put these three pictures in a folder and give the folder an appropriate name. Then become root and copy the folder to: 

`/usr/share/images/desktop-themes/* `

As last step, please run as root:	 

`update-desktop-theme -i`

Now the name of your folder should now be on the list of themes.


### Uninstall

Please use the command: 

`update-desktop-theme -r`

to reset the configuration files to the Debian default theme. Then uninstall the package by typing: 

`dpkg -r desktop-theme-kit`

![uninstall](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/uninstall.png)

Thanks for using the package.

---

## Future plans / Wishlist

For login-boxes or other messages, desktop-theme-kit comes with black, rounded elements. They are used by kdm, slim, grub theme and plymouth. 

![GUI-element](http://lazybrowndog.net/debian/desktop-theme-kit/screenshots/GUI-element.png)

I plan to do "add-on packages" that adds those elements in a different style.


---
 
# License

Copyright by Ulrich Hansen <uhansen@mainz-online.de> and Ronoaldo JLP <ronoaldo@gmail.com>, 2012, 2013. 

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110, USA
