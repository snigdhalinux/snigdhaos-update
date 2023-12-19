# Maintainer: TNE <tne@garudalinux.org>
# Maintainer: dr460nf1r3 <dr460nf1r3 at garudalinux dot org>

pkgname=garuda-update
pkgdesc="The Garuda Linux update command, in a separate package to allow separate updating"
pkgver=4.4.0
pkgrel=1
arch=('any')
license=('GPL')
depends=('coreutils' 'sed' 'gawk' 'pacman' 'wget')
backup=(etc/garuda/garuda-update/config)
source=("auto-pacman"
	"config"
	"garuda-update"
	"logrotate"
	"main-update"
	"update-helper-scripts")
sha512sums=('b3d1c8bdc27462d3c996806b12d2c9315d362bff051b188eaed72c568d0bade09018373b9fbd4d03ed90388f8cdff2e9262ce3fec50b261a9b98e8ce6644cfd0'
	'd5dbe3e4a47e9b5301d1e849c54f2632540f14878e6af4f11979d74fc0be1c36321229cf5128924251431087aa42c497c0ab57e0743973c9baaeccc24114e2e1'
	'f94ce4b40cdca33dd480d067041c8b9be9e0bc1c2e28862a00bb589f73acd1fce42a10859c02410711ea75a658c1773c07e613a8f0b6f8eb1a4b0a67036c54d8'
	'fd112c212c43d631740be11064e1fd4cc3023d0951e945445173def152e8930189575654ddac0eb34ffd6a2eb5670c47993aeda66ab8fa089583ec973026e7de'
	'586a12d25c8cd09b9a3552d5c00b4befc55eac8c0c35dac7d399b077dc8f86c3fda0a917fae13d2f449e12c661fb020598fa536738ce5714d6d19f43b08cad7c'
	'6529d283da520a577f996ef3aa8e1c9a7254c9e15f7d099b56062a9e3c6ac6eff499e782a78e2affab7c4d3191460a69c93aaf930a9266f8fb15f0cd0c879b2a')

package() {
	install -Dm755 garuda-update "$pkgdir"/usr/bin/garuda-update
	ln -s /usr/bin/garuda-update "$pkgdir"/usr/bin/update
	install -Dm755 update-helper-scripts "$pkgdir"/usr/lib/garuda/garuda-update/update-helper-scripts
	install -Dm755 main-update "$pkgdir"/usr/lib/garuda/garuda-update/main-update
	install -Dm755 auto-pacman "$pkgdir"/usr/lib/garuda/garuda-update/auto-pacman
	install -Dm644 logrotate "$pkgdir"/etc/logrotate.d/garuda-update
	install -Dm644 config "$pkgdir"/etc/garuda/garuda-update/config
}
