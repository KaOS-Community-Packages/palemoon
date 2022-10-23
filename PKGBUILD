pkgname=palemoon
pkgver=31.3.0.1
pkgrel=1
pkgdesc="Open source web browser based on Firefox focusing on efficiency."
arch=('x86_64')
url="https://linux.palemoon.org"
license=('MPL' 'GPL' 'LGPL')
depends=('gtk3' 'dbus-glib' 'desktop-file-utils' 'libxt' 'mime-types' 'nss' 'alsa-lib')
optdepends=('hunspell' 'hyphen')
install=${pkgname}.install
source=("https://linux.palemoon.org/datastore/release/${pkgname}-${pkgver}.linux-x86_64-gtk3.tar.xz"
        "${pkgname}.desktop"
        'changelog.html')
md5sums=('5ffebafca0229bd22aa124c14bbe9868'
         '0d4979b1746372fc2408bf76f146ae05'
         '36387222f698b3ceb423f60fd18f12c5')

package() {
    install -d ${pkgdir}/usr/{bin,lib}
    cp -r ${pkgname}/ ${pkgdir}/usr/lib/${pkgname}
    ln -s ../lib/${pkgname}/${pkgname} ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 changelog.html \
        ${pkgdir}/usr/share/${pkgname}/changelog.html
    
    local size
    for size in 16 32 48; do
        install -Dm644 ${pkgname}/browser/chrome/icons/default/default${size}.png \
                ${pkgdir}/usr/share/icons/hicolor/${size}x${size}/apps/${pkgname}.png
    done
    install -Dm644 ${pkgname}/browser/icons/mozicon128.png \
            ${pkgdir}/usr/share/icons/hicolor/128x128/apps/${pkgname}.png   

    rm -rf ${pkgdir}/usr/lib/${pkgname}/{dictionaries,hyphenation}
    
    ln -s /usr/share/hunspell ${pkgdir}/usr/lib/${pkgname}/dictionaries
    ln -s /usr/share/hyphen ${pkgdir}/usr/lib/${pkgname}/hyphenation
}
