# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: kitsunyan <kitsunyan@inbox.ru>
# Contributor: Grigorii Horos <horosgrisa@gmail.com>
# Modified by Frederic2ec for Namib

pkgname=papirus-icon-theme-namib
pkgbase=papirus-icon-theme
pkgver=20181120
pkgrel=1
pkgdesc="Papirus icon theme for Namib"
arch=('any')
url="https://github.com/PapirusDevelopmentTeam/papirus-icon-theme"
license=("LGPL3")
depends=('gtk-update-icon-cache')
source=("$pkgbase-$pkgver.tar.gz::https://github.com/PapirusDevelopmentTeam/$pkgbase/archive/$pkgver.tar.gz")
sha512sums=('430290d78a6f564eaab7a7a3a7b8fbe33c9ad14f69915f29b063c77e9452a1885e14d58dc472f347ed07da3fdd995e72528b65c3334bb7ba0e940a3da6e3f7dd')


prepare() {
	cd $pkgbase-$pkgver
	mv Papirus-Dark Papirus-Dark-Namib
	mv Papirus-Light Papirus-Light-Namib
	mv Papirus Papirus-Namib
	mv ePapirus ePapirus-Namib
  find ./ -type f -exec sed -i 's/5294e2/d64937/g' {} \;
  find ./ -type f -exec sed -i 's/4877b1/bf4b4b/g' {} \;
  find ./ -type f -exec sed -i 's/1d344f/4f1d1d/g' {} \;
}

package() {
  cd $pkgbase-$pkgver
  make DESTDIR="$pkgdir" install
}
