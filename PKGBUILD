# Maintainer: Levente Polyak <anthraxx[at]archlinux[dot]org>
# Contributor: Eric Bélanger <eric@archlinux.org>

pkgname=gajim
pkgver=1.2.0
pkgrel=1
pkgdesc='Full featured and easy to use XMPP (Jabber) client'
url='https://www.gajim.org/'
arch=('any')
license=('GPL3')
depends=('gtk3' 'python-cairo' 'python-gobject' 'python-keyring' 'python-nbxmpp'
         'python-pyasn1' 'python-pyopenssl' 'python-precis_i18n' 'python-cssutils'
         'python-css-parser' 'python-distro' 'hicolor-icon-theme')
optdepends=('alsa-utils: play notification sounds'
            'python-dbus: for gajim-remote and zeroconf support'
            'avahi: serverless chatting with autodetected clients in a local network'
            'farstream: start audio and video chat'
            'gst-plugins-good: for video/voice support'
            'gst-plugins-bad: for video/voice support'
            'gst-plugins-ugly: for video/voice support'
            'gst-libav: for video/voice support'
            'gst-python: for video/voice support'
            'gspell: for spell checking support'
            'notification-daemon: for desktop notifications'
            'geoclue2: share current location'
            'gnome-keyring: store passwords encrypted in GNOME Keyring'
            'kded: store passwords encrypted in KSecretService'
            'gupnp-igd: request your router to forward port for file transfer'
            'libxss: measure idle time, in order to set auto status'
            'python-crypto: encrypting chat messages'
            'python-docutils: generate XHTML output from RST code'
            'python-gnupg: encrypting chat messages with OpenPGP'
            'python-pillow: support of WebP avatars'
            'python-axolotl: OMEMO support'
            'python-qrcode: generate QR codes for OMEMO keys')
source=(https://www.gajim.org/downloads/${pkgver%.*}/gajim-${pkgver}.tar.gz)
sha512sums=('e73802dd1172c1fa38be10e6fb5d605109dacf0491516b15111ccd05389309af217e8af68440a1333b8a636c9ff425dec6d4461296ba47f1bb6dbb3000b02fd0')

build() {
  cd ${pkgname}-${pkgver}
  python setup.py build
}

package() {
  cd ${pkgname}-${pkgver}
  python setup.py install --root="${pkgdir}" --optimize=1 --skip-build
}

# vim: ts=2 sw=2 et:
