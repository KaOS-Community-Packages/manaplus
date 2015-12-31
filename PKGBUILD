pkgname=tmw
pkgver=1.5.12.19
pkgrel=1
pkgdesc="The Mana World (TMW) is a serious effort to create an innovative free and open source MMORPG."
arch=('x86_64')
url="http://themanaworld.org"
license=('GPL')
depends=( 'glu' 'curl' 'libgl' 'libxml2' 'physfs' 'zlib'
          'sdl' 'sdl_mixer' 'sdl1_ttf' 'sdl_image' 'sdl_net' )
makedepends=('mesa')
optdepends=('xsel')
#source=(http://downloads.sourceforge.net/sourceforge/themanaworld/$pkgname-$pkgver.tar.bz2)
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
