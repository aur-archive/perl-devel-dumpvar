#Maintainer: Simone Sclavi 'Ito' <darkhado@gmail.com>
pkgname=perl-devel-dumpvar
_realname=Devel-Dumpvar
pkgver=1.06
pkgrel=1
pkgdesc="A pure-OO reimplementation of dumpvar.pl"
arch=(any)
license=('GPL' 'PerlArtistic')
url="http://search.cpan.org/~adamk/Devel-Dumpvar"
options=(!emptydirs)
depends=('perl')

source=(http://search.cpan.org/CPAN/authors/id/A/AD/ADAMK/${_realname}-${pkgver}.tar.gz)
md5sums=('4a7e4d4fb9150e43c354fe674631ce1c')

build() {
  cd ${_realname}-${pkgver}
  perl Makefile.PL INSTALLDIRS=vendor
  make
}
check() {
  cd ${_realname}-${pkgver}
  make test
}
package(){
  cd ${_realname}-${pkgver}
  make install DESTDIR=${pkgdir}
}

