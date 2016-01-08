pkgname=nesasm3-git
pkgver=3.1r3.999d1e2
pkgrel=1
pkgdesc="Nintendo Entertaiment System assembler"
arch=('i686' 'x86_64')
url=""
license=('Freeware')
depends=('gcc')
conflicts=('nesasm3')
provides=('nesasm3')
source=("git+https://github.com/toastynerd/nesasm.git")
md5sums=('SKIP')

pkgver() {
  cd nesasm
  printf "3.1r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "$srcdir/nesasm"
  make
}

package() {
  cd "$srcdir/nesasm"
  install -d "$pkgdir/usr/bin"
  install -m755 $srcdir/nesasm/bin/* "$pkgdir/usr/bin/"
}
