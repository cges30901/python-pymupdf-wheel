# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
_py=cp39
pkgname=('python-pymupdf')
pkgver=1.18.9
pkgrel=1
pkgdesc='Python bindings for MuPDF'
arch=('x86_64')
url='https://github.com/pymupdf/PyMuPDF'
license=('AGPL3')
depends=('python>=3.9' 'python<3.10')
makedepends=('python-pip')

source=("https://files.pythonhosted.org/packages/$_py/${_name::1}/$_name/$_name-$pkgver-$_py-$_py-manylinux2010_x86_64.whl")
noextract=("${_name}-${pkgver}-$_py-$_py-manylinux2010_x86_64.whl")
sha256sums=('d554e5711dc6a3be67af9b8bcdd4093ad6bcc4081af319a0fb0433815df73f5e')

package() {
  cd "${srcdir}"
  export PIP_CONFIG_FILE=/dev/null
  pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-$_py-$_py-manylinux2010_x86_64.whl"
}
