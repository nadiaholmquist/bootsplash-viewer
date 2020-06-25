pkgname=bootsplash-viewer
pkgver=1.0
pkgrel=1
pkgdesc='Utility to view kernel bootsplash files'
arch=('i686' 'x86_64' 'aarch64')
url='https://github.com/philmmanjaro/linux-bootsplash'
license=('GPL2')
depends=('sdl2')
makedepends=('gcc')
source=(CMakeLists.txt bootsplash_file.h bootsplash-viewer.c)
md5sums=('5836033887727ff2a78e7de9feabf13a'
         'bf1ae5e25ab96db2d2b1ecfc40357ea8'
         'fcd74a0d4acda5bcfed45ae27f76b60d')

build() {
    cd "${srcdir}"

	mkdir -p build
	cd build

	cmake .. -DCMAKE_INSTALL_PREFIX="${pkgdir}/usr"
	make
}

package() {
    cd "${srcdir}/build"
	make install
}

# vim: ts=4 sw=4 et!:
