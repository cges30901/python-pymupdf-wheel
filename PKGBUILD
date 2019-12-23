# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
pkgname=('python2-pymupdf' 'python-pymupdf')
pkgver=1.16.10
pkgrel=1
pkgdesc='Python bindings for MuPDF'
arch=('x86_64')
url='https://github.com/pymupdf/PyMuPDF'
license=('AGPL3')
depends=('python2>=2.7' 'python2<2.8')
makedepends=('python2-pip' 'python-pip')

source=("https://files.pythonhosted.org/packages/cp27/${_name::1}/$_name/$_name-$pkgver-cp27-cp27mu-manylinux2010_x86_64.whl"
"https://files.pythonhosted.org/packages/cp38/${_name::1}/$_name/$_name-$pkgver-cp38-cp38-manylinux2010_x86_64.whl")
noextract=("${_name}-${pkgver}-cp27-cp27mu-manylinux2010_x86_64.whl"
           "${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl")
sha256sums=('af14719143d6a8240cb905dc74f05f8d77b56cad5740bd84e13ff077b8a88914'
            '027f7b3bb7d939ffea8cde925b1dd7723cd6c81dd053cef2a919d3f6b0d059e5')

package_python2-pymupdf() {
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip2 install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp27-cp27mu-manylinux2010_x86_64.whl"
}

package_python-pymupdf() {
  depends=('python>=3.8' 'python<3.9')
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl"
}
