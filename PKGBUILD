# $Id$
# Maintainer: Brian De Wolf <arch@bldewolf.com>
pkgname=gtkpass
pkgver=3
pkgrel=1
pkgdesc="Gtkpass is a GTK and Libkpass-based password manager for KeePass 1.x databases."
url="https://sourceforge.net/projects/gtkpass/"
arch=('i686' 'x86_64')
license=('GPL')
depends=('libkpass' 'gtk2')
makedepends=('pkgconfig' 'intltool')
conflicts=()
replaces=()
backup=()
source=(http://downloads.sourceforge.net/project/$pkgname/$pkgname-$pkgver/$pkgname-$pkgver.tar.gz)
md5sums=('496eb18a4ba3b16ab552390d5ecb11e3')
build() {
	cd "$srcdir/$pkgname-$pkgver"

	./configure --prefix=/usr
	make || return 1
}

package() {
	cd "$srcdir/$pkgname-$pkgver"

	make DESTDIR="$pkgdir/" install
}
