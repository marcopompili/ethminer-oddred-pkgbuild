# Maintainer: Marco Pompili <aur@mg.odd.red>
# Contributor: Afri 5chdn <aur@5chdn.co>
# Contributor: Andy Weidenbaum <archbaum@gmail.com>

pkgname=ethminer-oddred
pkgver=0.12.0
pkgrel=1
pkgdesc="Ethereum miner with OpenCL, CUDA and stratum support."
arch=('x86_64')
depends=(
  'boost'
  'boost-libs'
  'jsoncpp'
  'libjson-rpc-cpp-git'
  'opencl-headers'
  'python2'
)
optdeps=(
  'cuda: NVIDEA GPU mining support.'
  'opencl-mesa: AMD/ATI GPU mining support.'
)
url="https://github.com/ethereum-mining/ethminer"
license=('MIT')
source=(
  "https://github.com/ethereum-mining/ethminer/releases/download/v${pkgver}/ethminer-${pkgver}-Linux.tar.gz"
)
sha256sums=('be060bd78f9f0386b7a52f97d0c8b0bdc49941b2865e8ff77a0169bfd0b0b8af')
provides=(
  'ethminer'
)
conflicts=(
  'ethereum'
  'ethminer-git'
  'ethereum-git'
)

package() {
  install -Dm755 -t "${pkgdir}"/usr/bin ${srcdir}/bin/ethminer
}
