# Maintainer: Safwan Nayeem Yousuf <safwannayeemyousuf.com>
pkgname=firefox-theme-changer
pkgver=1
pkgrel=1
pkgdesc="Firefox theme changer"
arch=('any')
url="https://github.com/ramallahos/$pkgname"
license=('GPL')
depends=('yad' 'firefox' 'librewolf')
makedepends=('coreutils')
source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

package() {
    cd "$pkgname"
    install -d "$pkgdir/usr/bin/$pkgname-resources/"
    install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname-resources/$pkgname"
    install -Dm755 executable "$pkgdir/usr/bin/$pkgname"
    install -Dm755 *.svg "$pkgdir/usr/bin/$pkgname-resources/"
    install -Dm755 *.css "$pkgdir/usr/bin/$pkgname-resources/"
    install -Dm755 "$pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop"
}

