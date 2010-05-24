# Contributor: Thomas Mudrunka <harvie@@email..cz>
# Maintainer: Thomas Mudrunka <harvie@@email..cz>
# You can also contact me on http://blog.harvie.cz/

pkgname=aldm
pkgver=0.4
pkgrel=1
pkgdesc="ArchLinux Daemon Manager (Shell + Gnome GTK+ GUI) - Gives you control over services in rc.d and settings in rc.conf"
arch=('any')
license=('GPL')
url="http://aur.archlinux.org/packages.php?ID=29606"
depends=('bash' 'gtk2-perl' 'gksu' 'sed')
source=('aldm' 'aldm-gui' 'aldm.ui')
md5sums=('0c16113ad13f4e79c9b76ec22cf97206'
         '6a73ae72411eda426e9f97cfa1942fdd'
         'dd2f8a1d52200756edfb34afa5a574af')

build() {
	mkdir -p ${pkgdir}/usr/bin
	mkdir -p ${pkgdir}/usr/sbin
	mkdir -p ${pkgdir}/usr/share/aldm-gui

	cp -f ${srcdir}/aldm ${pkgdir}/usr/sbin/
	cp -f ${srcdir}/aldm-gui ${pkgdir}/usr/bin/
	cp -f ${srcdir}/aldm.ui ${pkgdir}/usr/share/aldm-gui

	mkdir -p ${pkgdir}/usr/share/applications

	echo '[Desktop Entry]
Encoding=UTF-8
Name=ArchLinux Daemon Manager
Comment=GTK frontend to ALDM
Comment[cs]=Grafické rozhraní pro ALDM
GenericName=System Services Manager
Type=Application
Exec=aldm-gui
Icon=server
Terminal=false
StartupNotify=false
Categories=Application;Settings;System;
' > ${pkgdir}/usr/share/applications/aldm-gui.desktop

	chmod -R 755 ${pkgdir}/
}
