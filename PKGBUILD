# Maintainer: Jimuel Palo <thewhat252@gmail.com>

_pkgver=3.3.1
_pkgrel=1
pkgname=dart
pkgver=${_pkgver}
pkgrel=${_pkgrel}
pkgdesc="The dart programming language SDK"
arch=("x86_64")
url="https://www.dartlang.org"
license=('BSD')
depends=('glibc')
provides=('dart')
conflicts=('dart')
source=("https://storage.googleapis.com/dart-archive/channels/stable/release/latest/linux_packages/dart_${_pkgver}-${_pkgrel}_amd64.deb")
md5sums=('SKIP')

build() {
    ar -x --  dart_${_pkgver}-${_pkgrel}_amd64.deb data.tar.xz
    tar -xvJf data.tar.xz
}

package() {
    cp -r $srcdir/usr $pkgdir
}
