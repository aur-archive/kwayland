# Maintainer: Antonio Rojas

pkgname=kwayland
pkgver=5.1.0.1
pkgrel=1
pkgdesc='Qt-style Client and Server library wrapper for the Wayland libraries'
arch=('i686' 'x86_64')
url='http://www.kde.org'
license=('LGPL')
depends=('qt5-base' 'wayland')
makedepends=('extra-cmake-modules')
source=("http://download.kde.org/stable/plasma/5.1.0/kwayland-$pkgver.tar.xz")
md5sums=('9e1e1192e77bb3312bf9adf867659abf')

prepare() {
  mkdir -p build
}

build() {
  cd build
  cmake ../$pkgname-5.1.0 \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DLIB_INSTALL_DIR=lib
  make
}

package() {
  cd build
  make DESTDIR="$pkgdir" install
}
