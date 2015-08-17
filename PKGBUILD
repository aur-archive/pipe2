# Maintainer: Thiago Perrotta <echo dGhpYWdvcGVycm90dGE5NUBnbWFpbC5jb20K | base64 -d >
# Contributor: Florian Walch <florian dot walch at gmx dot at>
# Contributor: thriqon <contact at jonasw de> 

pkgname=pipe2
_gitname=PIPE
pkgver=5.0.0
pkgrel=2
pkgdesc="Platform Independent Petri Net Editor."
arch=('i686' 'x86_64')
url="https://github.com/sarahtattersall/$_gitname"
license=('MIT')
depends=('java-runtime>=1.6')
makedepends=('maven' 'git')
provides=("pipe=${pkgver}")
conflicts=('pipe')
replaces=('pipe')
source=("git+https://github.com/sarahtattersall/$_gitname.git"
  "https://github.com/sarahtattersall/$_gitname/releases/download/$_gitname-$pkgver/$_gitname-gui-$pkgver.jar"
  pipe2)
md5sums=('SKIP'
         '02054d6c465bb5dd49e4d923fb2d1f52'
         '422296da5b1a095816fd491e8d98d9ec')
noextract=("$_gitname-gui-$pkgver.jar")

package() {
  cd "$srcdir"
  install -Dm755 "$_gitname-gui-$pkgver.jar" "${pkgdir}/usr/share/java/$pkgname/$_gitname-gui-$pkgver.jar"
  install -Dm755 pipe2 "${pkgdir}/usr/bin/pipe2"

  cd "$_gitname"
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
