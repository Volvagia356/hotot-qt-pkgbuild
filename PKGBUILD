_pkgname=Hotot
pkgname=hotot-qt
pkgver=20150628.1
pkgrel=1
arch=('i686' 'x86_64')
source=(git+https://github.com/Volvagia356/Hotot.git)
md5sums=(SKIP)

build() {
    cd "$srcdir/$_pkgname"
    mkdir build
    cd build
    cmake -DWITH_GTK=Off -DWITH_KDE=Off ..
    make
}

package() {
    cd "$srcdir/$_pkgname/build"
    make DESTDIR="$pkgdir" install
}
