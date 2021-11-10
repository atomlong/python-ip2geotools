# Maintainer: Atom Long <atom.long@hotmail.com>

_pkgname=ip2geotools
pkgname=python-${_pkgname}
pkgver=0.1.6
pkgrel=2
pkgdesc='Simple tool for getting geolocation information on given IP address from various geolocation databases.'
url='https://pypi.org/project/ip2geotools'
arch=('any')
license=('MIT')
depends=('python-dicttoxml' 'python-geocoder' 'python-geoip2' 'python-IP2Location' 'python-pyquery' 'python-requests'
         'python-selenium')
makedepends=('python-setuptools' 'python-pip')
checkdepends=('python-pytest' 'python-pytest-runner' 'python-pytest-mock' 'python-pytest-timeout' 'python-wheel')
source=("https://github.com/tomas-net/ip2geotools/archive/${pkgver}.tar.gz")
sha512sums=('3bbf33388409cce5b94cb79d28ac5d158796d27c6c23fc0609086299d94e41e5a396c4dc0f4b1f0e1becd3f8b887f09bf6b86b5f2651d2698ea6c48f1f7701ef')

build() {
  cd ${_pkgname}-${pkgver}
  python setup.py build
}

check() {
  cd ${_pkgname}-${pkgver}
  python setup.py test
}

package() {
  cd ${_pkgname}-${pkgver}
  python setup.py install --root="${pkgdir}" -O1 --skip-build
}

# vim: ts=2 sw=2 et:
