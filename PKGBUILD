# Contributer: giacomogiorgianni@gmail.com

pkgname=shoutcast_trans
pkgver=20111007
pkgrel=1
pkgdesc="Nullsoft SHOUTcast Streaming Client"
arch=('i686' 'x86_64')
url="http://www.shoutcast.com"
license=('custom')
depends=(gcc)
md5sums=('cbcd70d007ed8409546d96525650b8dc')
#source=(http://download.nullsoft.com/shoutcast/tools/sc_trans_linux_12_14_2010.tar.gz)
backup=(etc/sc_trans.conf)

if [ "${CARCH}" = 'x86_64' ]; then
    ARCH='linux_x64'
    source=(http://download.nullsoft.com/shoutcast/tools/sc_trans_linux_x64_10_07_2011.tar.gz)
    md5sums=('800489ee6e2dd23f75524e8dabc0f8b2')
  elif [ "${CARCH}" = 'i686' ]; then
    source=(http://download.nullsoft.com/shoutcast/tools/sc_trans_linux_10_07_2011.tar.gz)
    ARCH='linux'
    md5sums=('1eabe2716f5ab857a600dbd89d6192b6')
  fi


package() {
  install -D -m755 "$srcdir/sc_trans" "$pkgdir/usr/bin/shoutcast_trans"
  install -D -m644 "$srcdir/sc_trans_basic.conf" "$pkgdir/etc/sc_trans.conf"
}
