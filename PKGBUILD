pkgname=manaplus
pkgver=1.6.6.4
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
sha512sums=('962a149643415cd7a70ac5e73ca48931c8bd9588766e2d87aea2209d50c08f25994b710965161b504272eb334696433e9cf702e4451e188edea69298db25ccb3')

build() {
    cd ManaPlus-${pkgver}
    cmake . -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
    cd ManaPlus-${pkgver}
    make DESTDIR="$pkgdir" install
}
