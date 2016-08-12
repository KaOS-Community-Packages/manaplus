pkgname=manaplus
pkgver=1.6.7.30
pkgrel=1
pkgdesc="Advanced client for The Mana World and Evol Online (Mirror)"
arch=('x86_64')
url="http://manaplus.org/"
license=('GPL')
depends=( 'glu' 'curl' 'libgl' 'libxml2' 'physfs' 'zlib'
          'sdl' 'sdl_mixer' 'sdl1_ttf' 'sdl_image' 'sdl_net' )
makedepends=('mesa')
optdepends=('xsel')
source=("$pkgname-$pkgver.tar.gz::https://github.com/ManaPlus/ManaPlus/archive/v$pkgver.tar.gz")
sha512sums=('bbab86487e4dc857f03bdabe3830570d1cdc023772044ac307a9475c245a2a79e22307b8505db00fa0fd273fac66247a61704b92240d49a9578209c0846bcbf6')

build() {
    cd ManaPlus-${pkgver}
    cmake . -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd ManaPlus-${pkgver}
    make DESTDIR="$pkgdir" install
}
