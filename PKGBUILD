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
    mkdir -p "$pkgdir/usr/share/resources/$pkgname/"
    install -Dm755 "$pkgname" "$pkgdir/usr/share/resources/$pkgname/${pkgname}.sh"
    install -Dm755 executable "$pkgdir/usr/bin/$pkgname"
    cp -f *.svg "$pkgdir/usr/share/resources/$pkgname/"
    cp -f *.css "$pkgdir/usr/share/resources/$pkgname/"
    install -Dm755 "$pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop"
}

