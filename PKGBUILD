# Maintainer: Stefano Facchini <stefano.facchini@gmail.com>
pkgname=libvirt-glib
pkgver=0.1.6
pkgrel=1
pkgdesc="GLib bindings for libvirt"
arch=('i686' 'x86_64')
url="http://libvirt.org"
license=('LGPL2.1')
depends=('libvirt' 'glib2' 'gobject-introspection' 'python2')
options=('!libtool')
source=(ftp://libvirt.org/libvirt/glib/$pkgname-$pkgver.tar.gz)
sha256sums=('274b88584db94bb5d404e5398d6b5ef184afad49a2e4b3f4f6c47ba940bf55bf')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  PYTHON=/usr/bin/python2 ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
