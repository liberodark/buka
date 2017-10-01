# Maintainer: liberodark

pkgname=buka
pkgver=1.0.0
pkgrel=1
pkgdesc="EBook Management"
arch=('x86_64')
url="https://github.com/oguzhaninan/Buka"
license=('MIT')
depends=('xdg-utils')
source_x86_64=("https://github.com/oguzhaninan/Buka/releases/download/v1.0.0/Buka_1.0.0_amd64.deb")
source=($pkgname.desktop
        $pkgname.png)
sha512sums=('9b7626c9836d50d1f2bbb34fd0d89e8b7d07f28c2b4ef24df58afe4a998625802d8e870f35190f9f3fc8d19d694a4b7f31d98de2ea94827cda74cddb97174e52'
         'a506ffb7ce2dd6c8b91d3cc8c64609e8efc579872a54bf1ec8cc09c60156226442701fd56da1b218ce43ba1e37d05eb9b72b33a4dcc090b3bdccfb0926d0d18e')
sha512sums_x86_64=('133250429140ea711c37b5b2872410c5b6691b882680c0d74f88d52c7f8682d3fa11c1ae0a819ae7370d85ee4e38b1844c7a7c66c550ebe04dbf406d5e1701d9')
        
package() {
  cd $srcdir
  tar xvf data.tar.xz
  cp -r usr $pkgdir
  rm $pkgdir/usr/share/pixmaps/*.png
  rm $pkgdir/usr/share/applications/*.desktop
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/$pkgname.png
}
