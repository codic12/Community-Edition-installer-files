# Maintainer: Snehit Sah <snehitsah@protonmail.com>
# Contributor: The-Repo-Club <The-Repo-Club@github.com>
# Contributor: joekamprad <joekamprad@endeavourOS.com>

_pkgname=bspwm
pkgname=eos-skel-ce-bspwm
pkgver=1.0
pkgrel=13
pkgdesc="Pre user creation skel setup for Bspwm EOS-CE"
arch=('any')
groups=('eos-ce')
url="https://github.com/EndeavourOS-Community-Editions/${_pkgname}"
license=('GPL')
conflicts=('eos-ce-bspwm')
depends=('git')
source=("${_pkgname}::git+https://github.com/EndeavourOS-Community-Editions/${_pkgname}.git")
sha256sums=('SKIP')

package() {
    PREFIX=/etc/skel
    cd "$_pkgname"
    mkdir -p "${pkgdir}${PREFIX}/.config/"
    chmod +x .config/bspwm/bspwmrc
    chmod +x .config/polybar/*
    cp -R ".config/" "${pkgdir}${PREFIX}/"
    install -Dm644 ".gtkrc-2.0" "${pkgdir}${PREFIX}/.gtkrc-2.0"
    install -Dm644 "xed.dconf" "${pkgdir}${PREFIX}/xed.dconf"
    install -Dm644 "IosevkaTermNerdFontComplete.ttf" "${pkgdir}${PREFIX}/.local/share/fonts/IosevkaTermNerdFontComplete.ttf"
}
