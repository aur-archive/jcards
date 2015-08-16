# Maintainer: archtux <antonio dot arias99999 at gmail dot com>

pkgname=jcards
pkgver=6.5.1
pkgrel=1
pkgdesc="Easy user definable database program."
arch=('any')
url="http://www.nsydenham.net/java/JCards/JCards.shtml"
license=('GPL2')
depends=('java-runtime')
source=(http://www.nsydenham.net/java/JCards/v6/$pkgname$pkgver.zip
        http://www.nsydenham.net/java/JCards/jcards.png
        jcards
        jcards.desktop)
md5sums=('15a9a3e22bce98a86ee2481ce53f5149'
         'f80321b4c815dce56305ec4aabd37adf'
         'ed5a20e734dbda8fde934be1f51e539a'
         '0c175c96d81207ddea0be3b478ff9b1f')

package() {

   mkdir -p $pkgdir/usr/share
   cp -R $srcdir/JCards $pkgdir/usr/share
   rm  $pkgdir/usr/share/JCards/jcards.bat

   # Desktop icon
   install -Dm644 jcards.png $pkgdir/usr/share/pixmaps/jcards.png
   install -Dm644 jcards.desktop $pkgdir/usr/share/applications/jcards.desktop

   # Start file
   install -Dm755 jcards $pkgdir/usr/bin/jcards
}
