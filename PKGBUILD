pkgname=eos-systemd-boot
pkgver=0.9
pkgrel=1
pkgdesc='Enables systemd-boot automation using kernel-install on EndeavourOS'
arch=(any)
url='https://github.com/endeavouros-team/eos-systemd-boot'
license=(GPL2)
depends=(systemd)
source=(git+https://github.com/endeavouros-team/eos-systemd-boot.git)
sha256sums=('SKIP')

package()
{
    # install the package files
    cp -a ${srcdir}/${pkgname}/src/{usr,etc} ${pkgdir}

    # mask the default loaderentry creator
    mkdir -p "${pkgdir}/etc/kernel/install.d"
    touch "${pkgdir}/etc/kernel/install.d/90-loaderentry.install"
}
