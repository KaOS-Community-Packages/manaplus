pkgname=manaplus
pkgver=1.5.12.19
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
md5sums=('27555e5aa7797911de0c24d2fd97d587')

build() {
    cd $srcdir/ManaPlus-${pkgver}
    cmake . -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd $srcdir/ManaPlus-${pkgver}
    make DESTDIR="$pkgdir" install
}
