# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>
# Contributor: Maxwell Pray a.k.a. Synthead <synthead@gmail.com

_gemname=kgio
pkgname=ruby-$_gemname
pkgver=2.9.2
pkgrel=1
pkgdesc='kinder, gentler I/O for Ruby'
arch=(i686 x86_64)
url='http://bogomips.org/kgio/'
license=(LGPL2.1)
depends=(ruby)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('425e77117fa2eb70ae5d0f7cc517b9e2b3c50bcc')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/COPYING" "$pkgdir/usr/share/licenses/$pkgname/COPYING"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"

  rm -rf "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/ext"
}
