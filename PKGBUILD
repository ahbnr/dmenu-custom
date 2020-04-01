pkgname=dmenu-custom
pkgver=r573.b595e02
pkgrel=1
pkgdesc="Generic menu for X. With borders and centering patch."
arch=('x86_64')
url="https://tools.suckless.org/dmenu/"
license=('MIT')
provides=('dmenu')
conflicts=('dmenu')
depends=('sh' 'libxinerama' 'libxft' 'freetype2')

prepare() {
  cp -R $startdir/* $srcdir || true
}

build() {
  ./build.sh
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
