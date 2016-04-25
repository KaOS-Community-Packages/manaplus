pkgname=manaplus
pkgver=1.6.4.9
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
md5sums=('88a25d7cf442699ad2dc79039eeb54c2')

build() {
    cd $srcdir/ManaPlus-${pkgver}
    cmake . -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd $srcdir/ManaPlus-${pkgver}
    make DESTDIR="$pkgdir" install
}
