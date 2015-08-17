# Maintainer: Bartłomiej Piotrowski <bpiotrowski@archlinux.org>

pkgname=tt-rss-theme-reeder-git
pkgver=20140327
pkgrel=1
pkgdesc='Reeder like theme for Tiny Tiny RSS'
arch=('any')
url='https://github.com/tschinz/tt-rss_reeder_theme'
license=('CCPL:by-nc-nd')
depends=('tt-rss')
makedepends=('git')
source=($pkgname::git://github.com/tschinz/tt-rss_reeder_theme.git)
md5sums=('SKIP')

pkgver() {
  cd $pkgname
  git log -1 --format="%cd" --date=short | sed 's|-||g'
}

package() {
  cd $pkgname
  install -dm755 "$pkgdir"/usr/share/webapps/tt-rss/themes/
  install -Dm644 reeder.css "$pkgdir"/usr/share/webapps/tt-rss/themes/
  cp -r reeder "$pkgdir"/usr/share/webapps/tt-rss/themes/
}
