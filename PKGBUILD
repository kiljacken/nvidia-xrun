# Maintainer: Emil Lauridsen <mine809@gmail.com>
pkgname=nvidia-xrun-vfio
pkgver=0.3
pkgrel=0
epoch=
pkgdesc="Script to run dedicated X server with discrete nvidia graphics"
arch=("x86_64")
url="https://github.com/kiljacken/nvidia-xrun"
license=('GPL')
groups=()
depends=('xorg-server' 'xorg-xinit' 'xorg-xrandr' 'nvidia' 'mesa-libgl')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("nvidia-xorg.conf" "nvidia-xinitrc" "nvidia-xrun")
noextract=()
sha256sums=('9dfd296daed793d7da9dcf1ed48076c32c0131703e1527c36fa9a71aa6e673a7'
            'eed39d8fd44a5733bb05e70b3fe6882fe823a643bb19d7e714c197db34f8aa11'
            'df8627e8c116c6cb52944b909252eac7b0a33224be4f81c63dda2f96b55142f1')
validpgpkeys=()

package() {
	install -Dm 644 nvidia-xorg.conf "$pkgdir/etc/X11/nvidia-xorg.conf"
	install -Dm 644 nvidia-xinitrc "$pkgdir/etc/X11/xinit/nvidia-xinitrc"
	install -Dm 755 nvidia-xrun "$pkgdir/usr/bin/nvidia-xrun"
	install -dm 555 "$pkgdir/etc/X11/xinit/nvidia-xinitrc.d"
	install -dm 555 "$pkgdir/etc/X11/nvidia-xorg.conf.d"
}
