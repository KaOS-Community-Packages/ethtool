pkgname=ethtool
pkgver=5.4
pkgrel=1
epoch=1
pkgdesc="Utility for controlling network drivers and hardware"
arch=('x86_64')
url="https://www.kernel.org/pub/software/network/ethtool/"
license=('GPL')
depends=('glibc')
source=(https://www.kernel.org/pub/software/network/$pkgname/$pkgname-$pkgver.tar.xz)
sha1sums=('67113d5adf08ec0cb2a3cb3b5de63280de6f7f3b')

build() {
    cd $pkgname-$pkgver
    ./configure --prefix=/usr --mandir=/usr/share/man --sbindir=/usr/bin
    make
}

check() {
  cd $pkgname-$pkgver
  make check
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
