# Contributor: Tianjiao Yin <ytj000@gmail.com>

pkgname=boost-build-config
pkgdesc="boost-build auto configuration tool"
pkgver=20120529
pkgrel=4
arch=('i686' 'x86_64')
url="https://github.com/ytj/boost-build-config"
license=('WTFPLv2')
makedepends=('git')
install=boost-build.install
optdepends=(
	'qt: for qt support'
	'openmpi: for mpi support'
        'python: for python bindings'
	'python2: for python2 bindings'
	'docbook-xml: for boost book'
	'docbook-xsl: for boost book'
	'libxslt: for boost book'
	'doxygen: for boost book')

_gitroot=git://github.com/ytj/boost-build-config.git
_gitname="${srcdir}/conf"
build() {
    rm -rf "$_gitname"
    git clone --depth=1 $_gitroot $_gitname
    install -D -m755 "${_gitname}/boost-build-config" "${pkgdir}/usr/bin/boost-build-config"
    mkdir -p "${pkgdir}/etc/"
    touch "${pkgdir}/etc/site-config.jam"
}
