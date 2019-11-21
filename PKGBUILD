# Maintainer: Hsiu-Ming Chang <cges30901 at gmail dot com>
# Contributor: Ruikai Liu <lrk700 at gmail dot com>
# Contributor: Alexander Kobel <a-kobel at a-kobel dot de>

_name=PyMuPDF
pkgname=('python2-pymupdf' 'python-pymupdf')
pkgver=1.16.8
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
sha256sums=('73b1dd190306838e2ef9e1a5f5cc0a83c135ef5a48cc9793f321d25d2ee4361d'
            '89542dec97731c5ccfb3307af3ac1f7aa75ac1946e10a5a0948c2a72ed849ef8')

package_python2-pymupdf() {
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip2 install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp27-cp27mu-manylinux2010_x86_64.whl"
}

package_python-pymupdf() {
  depends=('python>=3.8' 'python<3.9')
  cd "${srcdir}"
  PIP_CONFIG_FILE=/dev/null pip install --isolated --root="$pkgdir" --ignore-installed --no-deps "${_name}-${pkgver}-cp38-cp38-manylinux2010_x86_64.whl"
}
