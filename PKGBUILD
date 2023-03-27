pkgname=galaxy-renderer
pkgdesc="application to visualize galxy simulation based on density wave theory"
pkgver=1.0.0
pkgrel=1
arch=("x86_64" "arm7h")
url="https://github.com/majorx234/Galaxy-Renderer"
license=("BSD-2")
depends=(sdl2 
  sdl2_ttf
  glm)
makedepends=(cmake gcc)
source=("git+https://github.com/majorx234/Galaxy-Renderer.git")
sha256sums=('SKIP')

build() {
[ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        ${srcdir}/Galaxy-Renderer
  make      
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}
