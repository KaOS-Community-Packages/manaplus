pkgname=manaplus
pkgver=1.6.4.23
pkgrel=1
pkgdesc="Advanced client for The Mana World and Evol Online (Mirror)"
arch=('x86_64')
url="http://manaplus.org/"
license=('GPL')
depends=( 'glu' 'curl' 'libgl' 'libxml2' 'physfs' 'zlib'
          'sdl' 'sdl_mixer' 'sdl1_ttf' 'sdl_image' 'sdl_net' )
makedepends=('mesa')
optdepends=('xsel')
source=(https://github.com/ManaPlus/ManaPlus/archive/v$pkgver.tar.gz)
sha512sums=('b27025b1db178366af12f9d68ffbb9a07225c9f637bc3ff96cb1e682a1a1816f6670696b2a6cc91701e68182186127daa0180054df1243aa352452b24d7c0ce6')

build() {
    cd $srcdir/ManaPlus-${pkgver}
    cmake . -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd $srcdir/ManaPlus-${pkgver}
    make DESTDIR="$pkgdir" install
}
