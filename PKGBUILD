# Maintainer: Gustavo Alvarez <sl1pkn07@gmail.com>

pkgname=emgdui
pkgver=1.8.0
_pkgver=1.0.1
pkgrel=3
pkgdesc="Driver configuration tool for the EMGD driver"
arch=('i686')
license=('custom')
url="http://edc.intel.com/Software/Downloads/EMGD/"
depends=('xproto' 'libxrandr' 'libx11' 'libpciaccess' 'dkms-emgd' 'xf86-video-emgd')
source=(https://launchpad.net/~gma500/+archive/emgd110/+files/${pkgname}_${pkgver}-${_pkgver}~oneiric.tar.gz)
md5sums=('257aec6312641a0e12e931ecd033f3ba')

build() {
     cd ${srcdir}/${pkgname}-${pkgver}/
     make     
}

package() {
     cd ${srcdir}/${pkgname}-${pkgver}/
     install -Dm755 emgdui ${pkgdir}/usr/bin/emgdui
     install -Dm755 Readme.txt ${pkgdir}/usr/share/doc/$pkgname/Readme.txt
     install -Dm755 sample_license.txt ${pkgdir}/usr/share/licenses/$pkgname/sample_license.txt
     install -Dm755 debian/emgdui.desktop ${pkgdir}/usr/share/applications/emgdui.desktop
} 
