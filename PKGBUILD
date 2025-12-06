pkgname=app
pkgver=1.0.0
pkgrel=1
pkgdesc="A c++ app to make mounting external drives easyer"
arch=('x86_64')
license=('MIT')
depends=('qt6-base')
makedepends=('qt6-base' 'qt6-tools' 'make' 'gcc')
source=("$pkgname-$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    qmake6
    make
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
}
