# Maintainer: Giancarlo Razzolini <grazzolini@gmail.com>
pkgname=mkinitcpio-ddns
pkgver=0.0.1
pkgrel=1
pkgdesc="This hook provides dynamic dns capabilities to the initramfs. It is meant for use with dropbear_initrd_encrypt and mkinitcpio-ppp for remote unlocking the luks root partition over the internet"
arch=('any')
url="https://github.com/grazzolini/mkinitcpio-ddns"
license=('BSD')
depends=('dropbear_initrd_encrypt', 'inadyn-mt')
install=$pkgname.install
source=('ChangeLog' "$pkgname.install" 'ddns_hook' 'ddns_install')
changelog='ChangeLog'
sha256sums=('6663f33155b4640f113539562fc7381583ae0e42ff680ee9425eae9ecd2dd7d0'
            '16c2ec0c45e3946e4310bd6ba96438630675efb53ab092540da7c287d3686a57'
            '256e89fab59da0d83dcb35e26041dbe9ee563989cf7c34a5b90be664d1cc5f1d'
            '896caa4bec27ebb4e1ca834dc6f5e7161c8030d7714091e0d8953826a64450a8')

package() {
  install -Dm644 "$srcdir/ddns_hook"      "$pkgdir/usr/lib/initcpio/hooks/ddns"
  install -Dm644 "$srcdir/ddns_install"   "$pkgdir/usr/lib/initcpio/install/ddns"
}
