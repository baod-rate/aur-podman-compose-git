# Maintainer: Alejandro Valdes <alejandrovaldes@live.com>
pkgname=podman-compose-git
_gitname="podman-compose"
pkgver=v0.1.5.r39.8c3b7e6
pkgrel=1
pkgdesc='a script to run docker-compose.yml using podman'
arch=('any')
url='https://github.com/containers/podman-compose'
license=('GPLv2')
depends=('python' 'python-yaml')
provides=("podman-compose")
conflicts=("podman-compose")
source=("git+https://github.com/containers/podman-compose.git")
sha256sums=('SKIP')

pkgver() {
  cd $srcdir/$_gitname
  printf "%s" "$(git describe --long | sed 's/\([^-]*-\)g/r\1/;s/-/./g')"
}

package() {
    cd $srcdir/$_gitname
    python setup.py install --root="${pkgdir}/" --optimize=1
}
