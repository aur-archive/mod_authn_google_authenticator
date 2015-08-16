# Maintainer: Arthur Darcet <arthur.darcet@m4x.org>

pkgname=mod_authn_google_authenticator
pkgver=0.1
pkgrel=2
pkgdesc='Apache module for two factor authentication using Google-Authenticator'
arch=('i686' 'x86_64')
url='http://code.google.com/p/mod-auth-external/'
license=('Apache')
makedepends=('apache')
install=mod_authn_google_authenticator.install
source=(http://google-authenticator-apache-module.googlecode.com/files/GoogleAuthApacheModule_v01.bz2)
md5sums=('99d08393ca116c6d0065aa3f5a46a45c')

build() {
  cd $srcdir/google-authenticator-apache-module
  make || return 1
  install -D -m755 .libs/mod_authn_google.so $pkgdir/usr/lib/httpd/modules/mod_authn_google_authenticator.so
}
