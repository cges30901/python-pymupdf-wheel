# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
_py=cp39
pkgname=('python-pymupdf')
pkgver=1.18.10
pkgrel=1
pkgdesc='Python bindings for MuPDF'
arch=('x86_64')
url='https://github.com/pymupdf/PyMuPDF'
license=('AGPL3')
depends=('python>=3.9' 'python<3.10')
makedepends=('python-pip')

source=("https://files.pythonhosted.org/packages/$_py/${_name::1}/$_name/$_name-$pkgver-$_py-$_py-manylinux2010_x86_64.whl")
noextract=("${_name}-${pkgver}-$_py-$_py-manylinux2010_x86_64.whl")
sha256sums=('cc8c1bec5c9175f21ced09b153e38c5d49ec2b4830d3e9289933c7eff1d4f367')

package() {
  cd "${srcdir}"
  export PIP_CONFIG_FILE=/dev/null
  pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-$_py-$_py-manylinux2010_x86_64.whl"
}
