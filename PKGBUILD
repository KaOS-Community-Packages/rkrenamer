pkgname=rkrenamer
pkgver=0.4.0
pkgrel=1
pkgdesc="Application for renaming large number of files"
arch=('x86_64')
url="http://karoljkocmaros.blogspot.com/p/rkrenamer.html"
license=('LGPL')
install=${pkgname}.install
depends=('qt5-base')
makedepends=('unzip')
source=(${pkgname}-${pkgver}.zip::"http://master.dl.sourceforge.net/project/${pkgname}/Source/${pkgver}/${pkgname}.zip") 
sha512sums=('b77838a1a857616bb7cdca9d6875bc4fe0c18fcc9f2caea7606ca7e8d71d52199d261dc04a85f68f6e962ccf5d35e44001865e41ea00b8946e707e4e00fa584b')

build(){
    cd trunk/
    qmake-qt5 PREFIX=/usr ${pkgname}.pro
    make DESTDIR="${pkgdir}"
}

package() {
 cd trunk/
 make INSTALL_ROOT="${pkgdir}" install
}
