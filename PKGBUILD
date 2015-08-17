pkgname=python-flask-principal
_pkgname=Flask-Principal
pkgver=0.3.5
pkgrel=1
pkgdesc='Identity management for flask (python3 version)'
arch=('i686', 'x86_64')
url="https://pypi.python.org/pypi/${_pkgname}"
license=('BSD')
depends=('python-flask')
source=("https://pypi.python.org/packages/source/F/${_pkgname}/${_pkgname}-${pkgver}.tar.gz")
md5sums=('8251576d89720119d23a4407c4ce8dc8')

build() {
    cd "$srcdir/${_pkgname}-${pkgver}"

    2to3 -wn . > /dev/null

    python setup.py build
}

package() {
    cd "$srcdir/${_pkgname}-${pkgver}"

    python setup.py install --root=${pkgdir} --optimize=1
}
