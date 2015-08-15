# Maintainer: Rich Lindsley <rich at dranek dot com>
pkgname=dame-git
_gitname=dame
pkgver=v0.5
pkgrel=1
pkgdesc="SIR image viewer"
arch=('any')
url="https://github.com/richli/dame"
license=('MIT')
depends=('libsir' 'python2-pyqt4' 'python2-numpy')
makedepends=('git' 'python2-setuptools')
provides=('dame')
conflicts=('dame')
source=('git://github.com/richli/dame')
md5sums=('SKIP') #generate with 'makepkg -g'

pkgver() {
  cd "$_gitname"
  git describe --always | sed 's|-|.|g'
}

package() {
  cd "$_gitname"
  python2 setup.py install --root="$pkgdir/" --optimize=1
  install -D -m644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
