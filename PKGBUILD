# Maintainer: Marco Pompili <aur@mg.odd.red>
# Contributor: Afri 5chdn <aur@5chdn.co>
# Contributor: Andy Weidenbaum <archbaum@gmail.com>

pkgname=ethminer-oddred
pkgver=0.18.0
pkgrel=1
pkgdesc="Ethereum miner with OpenCL, CUDA and stratum support."
arch=('x86_64')
depends=(boost boost-libs jsoncpp opencl-headers)
optdeps=(
  'cuda: NVidia GPU mining support.'
  'opencl-mesa: AMD/ATI GPU mining support.'
)
url="https://github.com/ethereum-mining/ethminer"
license=('MIT')
source=("https://github.com/ethereum-mining/ethminer/releases/download/v${pkgver}/ethminer-${pkgver}-cuda-9-linux-x86_64.tar.gz")
sha256sums=('98132b98c271ea1ad13796524996477f3a58c7c4a20182fe433f51e165a96642')
provides=('ethminer')
conflicts=('ethereum' 'ethminer-git' 'ethereum-git')
options=(!strip)

package() {
  install -Dm755 -t "${pkgdir}"/usr/bin "${srcdir}"/bin/ethminer
  cp -R "${srcdir}"/bin/kernels "${pkgdir}"/usr/bin
}
