# Maintainer: Frederik Schwan <frederik dot schwan at linux dot com>
# Contributor: Pablo Vilas <pablovilas89 at gmail dot com>
# Contributor: Testuser_01 <arch@nico-siebler.de>

pkgname=webstorm
_pkgname=WebStorm
pkgver=11.0.3
_pkgver=143.1559.5
pkgrel=1
pkgdesc="JavaScript IDE and HTML editor."
arch=('x86_64' 'i686')
options=('!strip')
url="http://www.jetbrains.com/${pkgname}/"
license=('Commercial')
depends=('java-environment>=6')
source=(https://download.jetbrains.com/webstorm/${_pkgname}-${pkgver}.tar.gz
        jetbrains-webstorm.desktop)
sha256sums=('387d2cf7fdd4ba4e1fb4bb223071d0bac6f5c254e014311cbf62b188448ba76b'
            'df1155779ec87c1f9e3237a2b79a0bea1242f4f2661d3d0f5f152ef24af93166')

package() {
  install -d -m 755 ${pkgdir}/opt/
  install -d -m 755 ${pkgdir}/usr/bin/
  install -d -m 755 ${pkgdir}/usr/share/applications/
  install -d -m 755 ${pkgdir}/usr/share/pixmaps/

  cp -a ${srcdir}/${_pkgname}-${_pkgver} $pkgdir/opt/${pkgname}

  ln -s /opt/$pkgname/bin/${pkgname}.sh $pkgdir/usr/bin/${pkgname}
  install -D -m 644 ${srcdir}/jetbrains-${pkgname}.desktop ${pkgdir}/usr/share/applications/
  install -D -m 644 "${pkgdir}/opt/${pkgname}/bin/${pkgname}.svg" "${pkgdir}/usr/share/pixmaps/${pkgname}.svg"
}
