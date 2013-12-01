![headline](screenshots/headline.png) 

The package desktop-theme-kit allows admins to customize the look of Debian GNU/Linux. In the past, graphics like wallpapers, login screens, lock screens or boot menus could be changed at various places and sometimes it was still hard to get it to work. 

Now the desktop-theme-kit can do this for you.


## The whole system with one look

| **Grub2** | **Grub2 Theme** | **Plymouth** |
|:--------:|:--------:|:--------:|
|[![roj-grubclassic](screenshots/roj-grubclassic-preview.png)](screenshots/roj-grubclassic.png)|[![roj-grubtheme](screenshots/roj-grubtheme-preview.png)](screenshots/roj-grubtheme.png)|[![roj-plymouth](screenshots/roj-plymouth-preview.png)](screenshots/roj-plymouth.png)|
| **GDM3** | **Gnome** | **KDM** |
|[![roj-gdm3](screenshots/roj-gdm3-preview.png)](screenshots/roj-gdm3.png)|[![roj-gnome](screenshots/roj-gnome-preview.png)](screenshots/roj-gnome.png)|[![roj-kdm](screenshots/roj-kdm-preview.png)](screenshots/roj-kdm.png)|
| **KSplash** | **KDE** | **slim** |
|[![roj-ksplash](screenshots/roj-ksplash-preview.png)](screenshots/roj-ksplash.png)|[![roj-kde](screenshots/roj-kde-preview.png)](screenshots/roj-kde.png)|[![roj-slim](screenshots/roj-slim-preview.png)](screenshots/roj-slim.png)|
| **lightdm** | **LXDE** | |
|[![roj-lightdm](screenshots/roj-lightdm-preview.png)](screenshots/roj-lightdm.png)|[![roj-lxde](screenshots/roj-lxde-preview.png)](screenshots/roj-lxde.png)||


## Six themes included - and easily add your own!

desktop-theme-kit comes with six themes:

| **Roj** | **Growing** | **Elegance Blue** |
|:--------:|:--------:|:--------:|
|[![Roj](screenshots/roj-gnome-preview.png)](screenshots/roj-wallpaper.png) | [![Elegance Blue](screenshots/elegance-blue-gnome-preview.png)](screenshots/elegance-blue-wallpaper.png)|[![Growing](screenshots/growing-gnome-preview.png)](screenshots/growing-wallpaper.png)|
| **Elegance Sepia** | **Jethro** | **Journey** |
|[![Elegance Sepia](screenshots/elegance-sepia-gnome-preview.png)](screenshots/elegance-sepia-wallpaper.png) | [![Jethro](screenshots/jethro-gnome-preview.png)](screenshots/jethro-wallpaper.png)|[![Journey](screenshots/journey-gnome-preview.png)](screenshots/journey-wallpaper.png)|

And you may VERY easily create your own themes! Just take a look into the chapter about [installation](#installation) a little bit further.

 
## How it works

Basically desktop-theme-kit is just pointing all necessary configuration files to the pictures you want to use, using Debian alternatives whenever possible.  

It also uses its own GUI elements (at the moment for kdm, slim, grub theme and plymouth).  

 

## Our users

desktop-theme-kit is supposed to unify the look of your desktop. It does that for **ALL** users of your system. 

So this is an instrument for admins, who want to have the same look and feel on all their Debian GNU/Linux systems for all users (for instance in a company or a lab).  

This is also a great tool for people who use Debian GNU/Linux as their desktop OS and want to see their favorite pictures on more than just the desktop wallpaper. 

 

## Who shouldn't use it 

People on multiuser systems, who just want to change their wallpaper. Not everybody wants to see your cat picture when they log in their system. :-) 

 

## [Installation](id:Installation)

Download [desktop-theme-kit*.deb] (downloads) and install it by using the command: 

`dpkg -i desktop-theme-kit*.deb` 

Afterwards please run our install script. This script changes the lines in various configuration files to point to our theme. Command (as root): 

`update-desktop-theme -i`

The script will show you a list of themes that are included in the desktop-theme-kit. Please choose one by typing its name. Afterwards log out and in (or reboot). 

 

## Using your own pictures

desktop-theme-kit comes with six themes included. But you may easily create your own: Only three picture files are needed: 

* A login picture (used by GDM3, KDM, Ksplash, slim, lightdm, 	grub theme and plymouth). The picture should be **1920x1080px**. 	The file should be named **login.png**. 

* A wallpaper (used by Gnome, KDE, XFCE). The preferred size is also **1920x1080px**. Please name the file **wallpaper.png**.  

* And the classic Grub bootscreen picture. The size should be **640x480px**. The file should be named **grub.png** 

At the moment only pictures in **PNG** format are allowed. Unfortunately not all programs accept SVG files. 

Now put these three pictures in a folder, give the folder a fitting name and copy the folder to: 

`/usr/share/images/desktop-themes/* `

As last step, please run again 

`update-desktop-theme -i`

The name of your folder should now be on the list of themes. Type it and voilà.


## Uninstall

Please use the command: 

`update-desktop-theme -r`

to reset the configuration files to the Debian default theme. Then uninstall the package by typing: 

`dpkg -r desktop-theme-kit`

Thanks for using the package.


---
 
# License

desktop-theme-kit 

Copyright by Ulrich Hansen <uhansen@mainz-online.de> and Ronoaldo JLP <ronoaldo@gmail.com>, 2012, 2013. 

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110, USA
