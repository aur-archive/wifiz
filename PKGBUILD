# Maintainer: Cody Dostal <dostalcody@gmail.com>

pkgname=wifiz
_gitname=WiFiz
pkgver=0.9.2.8.gc38cae9
pkgrel=2
pkgdesc="NetCTL GUI Frontend, written in wxPython. Stable Version."
arch=('any')
url="https://github.com/codywd/WiFiz"
license=('MIT')
depends=('python2' 'wxpython' 'wireless_tools' 'netctl' 
'wpa_supplicant')
makedepends=('git')
optdepends=('gedit: Manually editing profiles.')
conflicts=('wifiz-nightly')
provides=('wifiz')
source=('git://github.com/codywd/WiFiz.git#branch=develop')
# Because the sources are not static, skip Git checksum:
md5sums=('SKIP')

pkgver() {
  cd "$_gitname"
  echo $(git describe --long | sed 's/-/./g')
}

package() {
  cd $srcdir/$_gitname
  pwd
  python2 setup.py install --root="$pkgdir/" --optimize=1
}
