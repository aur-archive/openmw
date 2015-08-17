# Maintainer: Sandy Carter <bwrsandman@gmail.com>
# PKGBUILD source: https://github.com/bwrsandman/pkgbuild/tree/master/openmw

pkgname=openmw
pkgver=0.28.0
pkgrel=1
pkgdesc="An open-source engine reimplementation for the role-playing game Morrowind."
arch=('i686' 'x86_64')
url="http://www.openmw.org"
license=('GPL3' 'MIT' 'custom')

depends=('openal' 'ogre' 'mygui' 'bullet' 'qt4' 'ffmpeg' 'sdl2' 'unshield')
makedepends=('cmake' 'boost')

source=("https://github.com/zinnschlag/openmw/archive/${pkgname}-${pkgver}.tar.gz")
sha1sums=('2686b0a588571b9196e691b0ac484c59d8c49bce')

build() {
  cd "${srcdir}/${pkgname}-${pkgname}-${pkgver}"
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgname}-${pkgver}"
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
