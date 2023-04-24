# Maintainer: Erik Dubois <erik.dubois@gmail.com>
pkgname=arcolinux-alacritty-git
_pkgname=arcolinux-alacritty
_destname1="/etc/skel/.config/alacritty/"
_licensedir="/usr/share/arcolinux/licenses/"
pkgver=22.05
pkgrel=01
pkgdesc="Alacritty config for arcolinux"
arch=('any')
url="https://github.com/arcolinux/arcolinux-alacritty"
license=('GPL3')
makedepends=('git')
depends=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${_pkgname}::"git+https://github.com/arcolinux/${_pkgname}.git")
sha256sums=('SKIP')
install='readme.install'
package() {
	install -dm755 ${pkgdir}${_licensedir}${_pkgname}
	install -m644  ${srcdir}/${_pkgname}/LICENSE ${pkgdir}${_licensedir}${_pkgname}

	install -dm755 ${pkgdir}${_destname1}
	cp -r  ${srcdir}/${_pkgname}${_destname1}* ${pkgdir}${_destname1}
}



pkgname=rd_alacritty_config
_destname1="/"
pkgver=23.24
pkgrel=1
pkgdesc="Alacritty configuration file for Raindeer-OS"
arch=('any')
url="https://github.com/Raindeer-OS"
license=('GPL3')
makedepends=('git')
depends=()
conflicts=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${pkgname}::"git+${url}/${pkgname}")
sha256sums=('SKIP')
package() {
	install -dm755 ${pkgdir}${_destname1}
	cp -r ${srcdir}/${pkgname}${_destname1}/* ${pkgdir}${_destname1}
	rm ${pkgdir}${_destname1}/setup_git.sh
	rm ${pkgdir}${_destname1}/up.sh
	rm ${pkgdir}${_destname1}/README.md
	rm ${pkgdir}${_destname1}/LICENSE
	rm ${pkgdir}${_destname1}/PKGBUILD
}
