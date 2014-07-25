# Maintainer: tailinchu <use_my_id at gmail dot com>
# Contributor: reflexing <reflexing@reflexing.ru>

pkgname=ttf-noto
pkgver=20140725
pkgrel=1
pkgdesc="Google’s Unicode font family that aims to support all the world’s languages"
arch=('any')
url="http://www.google.com/get/noto"
license=('Apache')
depends=('fontconfig' 'xorg-fonts-encodings' 'xorg-mkfontscale' 'xorg-mkfontdir')
provides=('ttf-font')
source=("http://www.google.com/get/noto/pkgs/Noto-hinted.zip")
md5sums=('e72d000d9e90729a6caceff7afaf1f45')
install=$pkgname.install
PKGEXT='.pkg.tar' # because XZ compression is awfully slow

package() {
    # Prepare destination directories
    install -dm755 "$pkgdir"/usr/share/fonts/{TTF,OTF}

    # Install fonts
    install -m644 *.ttf "$pkgdir/usr/share/fonts/TTF"
    install -m644 *.otf "$pkgdir/usr/share/fonts/OTF"
}
