# Maintainer: bash-ful <bash-ful0931@proton.me>

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
source=("https://storage.googleapis.com/dart-archive/channels/stable/release/${_pkgver}/sdk/dartsdk-linux-x64-release.zip")
sha256sums=('1b1016fdeeb2037d181bedf3a5674f526f5a0ecb1bc97ed479dbfdbfc5a6d756')

build() {
    unzip -u -- dartsdk-linux-x64-release.zip
}

package() {
    srcdir_sub="$srcdir/dart-sdk"
    for file in $(find $srcdir_sub -type f) ; do
        install -Dm644 "${file}" "$pkgdir/usr/${file#$srcdir_sub/}"
    done
    echo $PWD
    install -Dm755 "dart-sdk/bin/dart" "$pkgdir/usr/bin/"
}
