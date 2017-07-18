pkgname=palemoon
pkgver=27.4.0
pkgrel=1
pkgdesc="Open source web browser based on Firefox focusing on efficiency."
arch=('x86_64')
url="https://linux.palemoon.org"
license=('MPL' 'GPL' 'LGPL')
depends=('gtk2' 'dbus-glib' 'desktop-file-utils' 'libxt' 'mime-types' 'nss' 'alsa-lib')
optdepends=('hunspell' 'hyphen')
install=${pkgname}.install
source=("${pkgname}-${pkgver}.en-US.linux-x86_64.tar.bz2::${url}/installer/download.php?v=${pkgver}&a=x86_64"
        "${pkgname}.desktop"
        'changelog.md')
md5sums=('66d193ee1bc306d3e25ae31fc3eaccaa'
         '0d4979b1746372fc2408bf76f146ae05'
         'bd79067d247fe0e2cc7526647ed2566b')

package() {
    install -d ${pkgdir}/usr/{bin,lib}
    cp -r ${pkgname}/ ${pkgdir}/usr/lib/${pkgname}
    ln -s ../lib/${pkgname}/${pkgname} ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 changelog.md \
        ${pkgdir}/usr/share/${pkgname}/changelog.md
    
    local size
    for size in 16 32 48; do
        install -Dm644 ${pkgname}/browser/chrome/icons/default/default${size}.png \
                ${pkgdir}/usr/share/icons/hicolor/${size}x${size}/apps/${pkgname}.png
    done
    install -Dm644 ${pkgname}/browser/icons/mozicon128.png \
            ${pkgdir}/usr/share/icons/hicolor/128x128/apps/${pkgname}.png   

    rm -rf "${pkgdir}"/usr/lib/${pkgname}/{dictionaries,hyphenation}
    
    ln -s /usr/share/hunspell ${pkgdir}/usr/lib/${pkgname}/dictionaries
    ln -s /usr/share/hyphen ${pkgdir}/usr/lib/${pkgname}/hyphenation
    ln -sf ${pkgname} ${pkgdir}/usr/lib/${pkgname}/${pkgname}-bin
}
