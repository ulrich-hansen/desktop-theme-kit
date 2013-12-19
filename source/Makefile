#
# Generic Makefile for building a Debian theme
#

# THEME CONFIG BEGIN

THEME=kit
PACKAGE=desktop-theme-package
ARTWORK_FOLDER=desktop-themes

# THEME CONFIG END


INSTALL=install -m 0644

init:
	mkdir -p backgrounds debian gdm3 grub kde-wallpaper kdm-theme ksplash plymouth readme

clean:
	

build:
	
	
mkdirs:
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/backgrounds/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/gdm3/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/grub/theme-black/icons/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/kde-wallpaper/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/kdm-theme/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/ksplash/
	mkdir -p $(DESTDIR)/usr/share/desktop-theme-$(THEME)/readme/
	mkdir -p $(DESTDIR)/usr/share/plymouth/themes/$(THEME)/
	mkdir -p $(DESTDIR)/etc/default/kdm.d/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1024x768/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1280x1024/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1280x800/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1366x768/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1600x1200/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1920x1080/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1920x1200/
	mkdir -p $(DESTDIR)/usr/share/kde4/apps/kdm/themes/$(THEME)/
	mkdir -p $(DESTDIR)/usr/share/wallpapers/$(THEME)/contents/images/
	mkdir -p $(DESTDIR)/usr/share/gnome-background-properties/
	mkdir -p $(DESTDIR)/etc/xdg/autostart/
	mkdir -p $(DESTDIR)/usr/bin/
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/growing
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/elegance-blue
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/elegance-sepia
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/jethro
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/roj
	mkdir -p $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/journey
	mkdir -p $(DESTDIR)/usr/share/slim/themes/$(PACKAGE)/
	mkdir -p $(DESTDIR)/usr/share/man/man8
	

install-backgrounds: mkdirs
	$(INSTALL) backgrounds/$(THEME)-wallpaper.png $(DESTDIR)/usr/share/desktop-theme-$(THEME)/backgrounds/
	$(INSTALL) backgrounds/$(THEME)-login.png $(DESTDIR)/usr/share/desktop-theme-$(THEME)/backgrounds/
	$(INSTALL) backgrounds/$(THEME)-gnome-backgrounds.xml $(DESTDIR)/usr/share/gnome-background-properties/$(THEME).xml
	$(INSTALL) backgrounds/$(THEME)-gnome-lockscreen.xml $(DESTDIR)/usr/share/desktop-theme-$(THEME)/backgrounds/


install-plymouth: mkdirs
	$(INSTALL) $(wildcard plymouth/*) $(DESTDIR)/usr/share/plymouth/themes/$(THEME)/


install-grub: mkdirs
	$(INSTALL) $(wildcard grub/*.* ) $(DESTDIR)/usr/share/desktop-theme-$(THEME)/grub
	$(INSTALL) $(wildcard grub/theme-black/*.*) $(DESTDIR)/usr/share/desktop-theme-$(THEME)/grub/theme-black
	$(INSTALL) $(wildcard grub/theme-black/icons/*.*) $(DESTDIR)/usr/share/desktop-theme-$(THEME)/grub/theme-black/icons


install-gdm3: mkdirs
	$(INSTALL) gdm3/$(THEME)-gdm3-background.conf $(DESTDIR)/usr/share/desktop-theme-$(THEME)/gdm3/


install-ksplash: mkdirs
	$(INSTALL) $(wildcard ksplash/theme/*.*) $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/
	$(INSTALL) $(wildcard ksplash/theme/1920x1080/*) $(DESTDIR)/usr/share/kde4/apps/ksplash/Themes/$(THEME)/1920x1080/
	$(INSTALL) ksplash/$(THEME)-ksplash.conf $(DESTDIR)/usr/share/desktop-theme-$(THEME)/ksplash/


install-kdm: mkdirs
	$(INSTALL) kdm-theme/$(THEME)-kdm.conf $(DESTDIR)/usr/share/desktop-theme-$(THEME)/kdm-theme/
	$(INSTALL) $(wildcard kdm-theme/theme/*.*) $(DESTDIR)/usr/share/kde4/apps/kdm/themes/$(THEME)/


install-kde: mkdirs
	$(INSTALL) kde-wallpaper/theme/metadata.desktop $(DESTDIR)/usr/share/wallpapers/$(THEME)/
	$(INSTALL) kde-wallpaper/theme/contents/screenshot.png $(DESTDIR)/usr/share/wallpapers/$(THEME)/contents/
#	$(INSTALL) $(wildcard kde-wallpaper/theme/contents/images/*) $(DESTDIR)/usr/share/wallpapers/$(THEME)/contents/images/
	$(INSTALL) kde-wallpaper/$(THEME)-kde-wallpaper.conf $(DESTDIR)/usr/share/desktop-theme-$(THEME)/kde-wallpaper/

install-slim: mkdirs
	$(INSTALL) $(wildcard slim/*) $(DESTDIR)/usr/share/slim/themes/$(PACKAGE)/

install-readme: mkdirs
	$(INSTALL) $(wildcard readme/*) $(DESTDIR)/usr/share/desktop-theme-$(THEME)/readme/


install-script: mkdirs
	$(INSTALL) script/update-desktop-theme $(DESTDIR)/usr/bin/update-desktop-theme

install-manpage: mkdirs
	$(INSTALL) script/update-desktop-theme.8.gz $(DESTDIR)/usr/share/man/man8/update-desktop-theme.8.gz

install-themes: mkdirs
	$(INSTALL) $(wildcard themes/growing/*.* ) $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/growing/
	$(INSTALL) $(wildcard themes/roj/*.* ) $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/roj/
	$(INSTALL) $(wildcard themes/journey/*.* ) $(DESTDIR)/usr/share/images/$(ARTWORK_FOLDER)/journey/


install: install-backgrounds install-plymouth install-grub install-gdm3 install-ksplash install-kdm install-kde install-readme install-slim install-script install-themes install-manpage
	
