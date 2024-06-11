pkgname=st
pkgver=1.0
pkgrel="$(date +%Y%m%d%H%M%S)"
epoch=
pkgdesc='Suckless Terminal (JMW build)'
arch=('any')
url='https://github.com/Jacajack/st'
license=('MIT')
groups=()
depends=()
optdepends=()
provides=()
conflicts=()
replaces=()
options=()
source=('git+https://github.com/jacajack/st')
cksums=(SKIP)

prepare() {
	:
}

check() {
	:
}

package() {
	make -C st -j
	make -C st install DESTDIR="$pkgdir"
	mkdir -p "$pkgdir/usr/share/st"
	cp "st/st.info" "$pkgdir/usr/share/st"
}

post_install() {
	tic -sx "/usr/share/st/st.info"
}
