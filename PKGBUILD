# Maintainer: szoltysek <karolszoltysek.ti@gmail.com>
# Fork by: Aduss404

pkgname=fossierglaze-git
pkgver=1.1.r8.g5909461
pkgrel=1
pkgdesc="Rub your Linux distro into every Discord user's face via Discord RPC with extended compatibility."
arch=('any')
url="https://github.com/Aduss404/fossierglaze/"
license=('GPL3')
depends=('python' 'python-pypresence')
makedepends=('git')
provides=('fossierglaze')
conflicts=('fossierglaze')
source=("git+${url}#branch=main")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/fossierglaze"
  # Generate version string like: 1.0.rXX.gabcdef
  printf "1.1.r%s.g%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/fossierglaze"

  # Install the Python script as an executable
  install -Dm755 fossierglaze.py "$pkgdir/usr/bin/fossierglaze"

  # Install documentation and license
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
}
