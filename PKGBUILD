pkgname=rebuild
pkgver=0.14
pkgrel=1
pkgdesc="A build tool for the D programming language"
arch=(i686 x86_64)
depends=()
url="http://dsource.org/projects/dsss/wiki/Rebuild"
source=(http://svn.dsource.org/projects/dsss/downloads/$pkgname/$pkgver/$pkgname-$pkgver.tar.bz2 makefix.patch)
md5sums=()

build() {
  cd ${startdir}/src/${pkgname}-${pkgver}

  patch -p1 <../makefix.patch

  make || return 1
  make DESTDIR=${startdir}/pkg install
}
