# Maintainer: Roland Singer <roland@manjaro.org>

pkgname=devtools
pkgver=20141224
pkgrel=1
pkgdesc='Tools for Manjaro Linux package maintainers'
arch=('any')
license=('GPL')
url='http://git.manjaro.org/core/devtools/'
depends=('namcap' 'openssh' 'subversion' 'rsync' 'arch-install-scripts')
source=("git+https://github.com/manjaro/devtools.git")
sha256sums=('SKIP')

pkgver() {
	date +%Y%m%d
}

build() {
	cd ${srcdir}/${pkgname}
	make PREFIX=/usr
}

package() {
	cd ${srcdir}/${pkgname}
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
