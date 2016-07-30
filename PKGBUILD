# Maintainer: Marcel Hasler <mahasler at gmail dot com>

pkgname=scilab-bin
pkgver=1469538020
_pkgdate=2016-07-30
pkgrel=1
pkgdesc="A scientific software package for numerical computations."
arch=("x86_64")
license=("BSD" "custom:CeCILL")
url="https://www.scilab.org"
source=("scilab.sh"
"scilab-master-$pkgver.tar.gz::http://downloadarea.scilab.org/download/$_pkgdate/scilab-master-$pkgver.bin.linux-x86_64.tar.gz")
sha512sums=('798c187a10ce5ec033ae0e462b4e70a11ccee3509920b4dfade4bb5fe3de4233a8f822f1b4a1ea3ba13a9212a851dca1d6a1382c41d688eb2343d60648299e85'
            'd647db45d8ff7b7087774aad80f6adb2b43a6da9ba8a2ddf80f1234e3e5232405037a1bed282774b0aaf4586b6d92ed3ef56e0dd8ccfbf84604e73e184cd012a')

package() {
  cd "${srcdir}"

  install -d "${pkgdir}/opt"
  cp -r "${srcdir}/scilab-master-${pkgver}" "${pkgdir}/opt/scilab"

  install -Dm 644 "${srcdir}/scilab-master-${pkgver}/COPYING" "${pkgdir}/usr/share/licenses/${pkgname}/COPYING"

  install -d "${pkgdir}/usr/share/applications"
  install -Dm 644 "${srcdir}/scilab-master-${pkgver}/share/applications/scilab.desktop" "${pkgdir}/usr/share/applications/scilab.desktop"

  install -d "${pkgdir}/usr/share/icons"
  cp -r "${srcdir}/scilab-master-${pkgver}/share/icons/hicolor" "${pkgdir}/usr/share/icons/"

  install -Dm 755 scilab.sh "${pkgdir}/usr/bin/scilab"
}
