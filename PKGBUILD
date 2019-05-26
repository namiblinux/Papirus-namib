# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: kitsunyan <kitsunyan@inbox.ru>
# Contributor: Grigorii Horos <horosgrisa@gmail.com>
# Modified by Frederic2ec for Namib

pkgname=papirus-icon-theme-namib
pkgbase=papirus-icon-theme
pkgver=20190521
pkgrel=1
pkgdesc="Papirus icon theme for Namib"
arch=('any')
url="https://github.com/PapirusDevelopmentTeam/papirus-icon-theme"
license=("LGPL3")
depends=('gtk-update-icon-cache')
source=("$pkgbase-$pkgver.tar.gz::https://github.com/PapirusDevelopmentTeam/$pkgbase/archive/$pkgver.tar.gz")
sha512sums=('d5c33ce976d426f8ebe250714a4a0fabe6c0202579b62d0444c3881dab80d468bd3f92632dd05b0aea570646fc330f5f3a67650482e2044c490622294e5c2adb')


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
