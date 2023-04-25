# Raindeer-OS Alacritty terminal theme config
pkgname=rd_alacritty_config
_destname1="/"
pkgver=23.25
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
