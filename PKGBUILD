# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
pkgname=('python-pymupdf')
pkgver=1.16.11
pkgrel=1
pkgdesc='Python bindings for MuPDF'
arch=('x86_64')
url='https://github.com/pymupdf/PyMuPDF'
license=('AGPL3')
depends=('python>=3.8' 'python<3.9')
makedepends=('python-pip')

source=("https://files.pythonhosted.org/packages/cp38/${_name::1}/$_name/$_name-$pkgver-cp38-cp38-manylinux2010_x86_64.whl")
noextract=("${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl")
sha256sums=('2adb6ee93f30cf06ba519bcf0059f1b19d184bd13bfc5b4aee915ebc566dffef')

package() {
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl"
}
