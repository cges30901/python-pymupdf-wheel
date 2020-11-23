# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
pkgname=('python-pymupdf')
pkgver=1.18.4
pkgrel=1
pkgdesc='Python bindings for MuPDF'
arch=('x86_64')
url='https://github.com/pymupdf/PyMuPDF'
license=('AGPL3')
depends=('python>=3.8' 'python<3.9')
makedepends=('python-pip')

source=("https://files.pythonhosted.org/packages/cp38/${_name::1}/$_name/$_name-$pkgver-cp38-cp38-manylinux2010_x86_64.whl")
noextract=("${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl")
sha256sums=('c894283f067077d02e2d4c6fc05317ab57f5955973016b75876980ea3487ee15')

package() {
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl"
}
