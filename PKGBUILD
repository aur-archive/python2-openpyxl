#Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
#Contributor: Martin Corley <Martin.Corley@ed.ac.uk>

pkgname=python2-openpyxl
pkgver=2.1.2
pkgrel=1
pkgdesc="A Python library to read/write Excel 2007 xlsx/xlsm files, 2.x branch"
arch=('any')
url="http://openpyxl.readthedocs.org/"
license=('MIT')
depends=('python2-jdcal' 'python2-lxml')
optdepends=('python2-pillow: needed to include images')
makedepends=('python2-setuptools')
source=("https://pypi.python.org/packages/source/o/openpyxl/openpyxl-${pkgver}.tar.gz"
        "LICENCE")
md5sums=('7a436a938bd19cd36942870ca3183034'
         'c8afe530744e932b892358e6eb5bea9b')
conflicts=('python2-openpyxl1')

build() {
  cd "$srcdir"/openpyxl-${pkgver}
  python2 setup.py build
}

package() {
  cd "$srcdir"/openpyxl-${pkgver}

  python2 setup.py install --skip-build --root="$pkgdir" --optimize=1

  install -Dm644 "$srcdir"/LICENCE "$pkgdir"/usr/share/licenses/$pkgname/LICENCE
}

