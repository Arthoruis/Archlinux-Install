# Maintainer: Arthorius <Arthcomicando@gmail.com>

pkgname=my-dotfiles
pkgver=1.0
pkgrel=1
pkgdesc="My dotfiles on skel folder"
arch=(x86_64)
url="https://github.com/Arthoruis/i3-dotfiles"
license=('GPL3')
depends=('git')
makedepends=('git' 'unzip')
install=my-dotfiles.install
source=(git+https://github.com/Arthoruis/i3-dotfiles.git)
md5sums=('SKIP')

package() {
	cd "${srcdir}/i3-dotfiles/"
	mkdir -p "${pkgdir}/etc/skel/Pictures/Screen-Capture/"
	mkdir -p "${pkgdir}/etc/skel"
	mkdir -p "${pkgdir}/etc/skel/Clamscan/"
	mkdir -p "${pkgdir}/usr/share/backgrounds/"
	cp -rf ".bash-scripts/" "${pkgdir}/etc/skel"
	cp -rf ".config/" "${pkgdir}/etc/skel/"
	cp -rf ".local/" "${pkgdir}/etc/skel/"
	cp -rf "Pictures/Wallpapers/" "${pkgdir}/usr/share/backgrounds/my-wallpapers/"
	cp -rf "Templates" "${pkgdir}/etc/skel/"
	install -Dm 0644 ".bash_profile" "${pkgdir}/etc/skel/.bash_profile1"
	install -Dm 0644 ".bashrc" "${pkgdir}/etc/skel/.bashrc1"
	install -Dm 0644 ".conkyrc" "${pkgdir}/etc/skel/"
	install -Dm 0644 ".Xdefaults" "${pkgdir}/etc/skel/"
	install -Dm 0644 ".xinitrc" "${pkgdir}/etc/skel/"
}
