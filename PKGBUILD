# Maintainer: Todd Partridge <https://github.com/Gen2ly/archpkgs>

pkgname=gently-bashrc-git
_pkgname=${pkgname%-*}
pkgver=1.0.0
pkgrel=1
pkgdesc="A bash configuration file meant to replace a local ~/.bashrc."
arch=("any")
url="https://github.com/Gen2ly/$_pkgname"
license=("GPL2")
depends=("bash")
makedepends=("git")
install=${_pkgname}.install
source=("git://github.com/Gen2ly/$_pkgname")
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  git describe --long | sed -r 's/-([0-9,a-g,A-G]{7}.*)//' | sed 's/-/./'
}

package() {
  cd $srcdir/$_pkgname
  install -Dm644 ${_pkgname/-/.} $pkgdir/usr/share/doc/$_pkgname/${_pkgname/-/.}
  install -Dm644 license.txt     $pkgdir/usr/share/licenses/$_pkgname/license.txt
}

# vim:set ts=2 sw=2 et:
