pkgname=eos-systemd-boot
pkgver=0.01
pkgrel=1
pkgdesc='Enables systemd-boot automation using kernel-install on EndeavourOS'
arch=(any)
url='https://gitlab.com/dalto.8/eos-systemd-boot'
license=(GPL2)
depends=(systemd)
source=(git+https://gitlab.com/dalto.8/eos-systemd-boot.git)
sha256sums=('SKIP')

package()
{
    # install the package files
    cp -a src/* "${pkgdir}"

    # mask the mkinitcpio hooks
    touch "${pkgdir}/etc/pacman.d/hooks/90-mkinitcpio-install.hook"
    touch "${pkgdir}/etc/pacman.d/hooks/60-mkinitcpio-remove.hook"
}
