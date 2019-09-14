 # Maintainer: Patrick Young <16604643+kmahyyg@users.noreply.github.com>
pkgname=dptech-sslvpn
pkgver=7.1.0
pkgrel=1
depends=('openssl098')
conflicts=('mxml')
pkgdesc="Fucking Damn SSL VPN offered by Zhejiang DPTech, Built for YNU"
arch=('x86_64')
url="https://ssl.ynu.edu.cn/"
license=('custom')
options=("!strip")

source=(
    "dpsslvpn.tar.gz"
)
sha256sums=(
    "3ad5b4d8ca640e28f474e4aefe61787a59c8cea0c61c18c412eeb77c6ad1a388"
)

package() {
    install -Dm755 "sslvpn_client_linux64" "${pkgdir}/usr/bin/dpsslvpn"
    install -Dm644 "etc/sslvpn.conf" "${pkgdir}/etc/sslvpn.conf"
    install -Dm644 "usr/lib/libSSLVPNSDK.so" "${pkgdir}/usr/lib/libSSLVPNSDK.so"
    install -Dm644 "usr/lib/libSSLVPNPlugin.so" "${pkgdir}/usr/lib/libSSLVPNPlugin.so"
    install -Dm644 "usr/lib/libSSLVPNCrypto.so" "${pkgdir}/usr/lib/libSSLVPNCrypto.so"
    install -Dm644 "usr/lib/libmxml.so" "${pkgdir}/usr/lib/libmxml.so"
    install -Dm644 "usr/lib/libmxml.so.1" "${pkgdir}/usr/lib/libmxml.so.1"
}
