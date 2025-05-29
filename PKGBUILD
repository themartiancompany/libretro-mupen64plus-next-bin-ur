# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2025  Pellegrino Prevete
#
#    All rights reserved
#    ----------------------------------------------------------------------
#
#    This program is free software: you can redistribute it and/or modify
#    it under the terms of the GNU Affero General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    This program is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU Affero General Public License for more details.
#
#    You should have received a copy of the GNU Affero General Public License
#    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# Maintainer:
#   Truocolo
#     <truocolo@aol.com>
#     <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
# Maintainer:
#   Pellegrino Prevete (dvorak)
#     <pellegrinoprevete@gmail.com>
#     <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>

_os="$( \
  uname \
    -o)"
_evmfs_available="$( \
  command \
    -v \
    "evmfs" || \
    true)"
if [[ ! -v "_evmfs" ]]; then
  if [[ "${_evmfs_available}" != "" ]]; then
    _evmfs="true"
  elif [[ "${_evmfs_available}" == "" ]]; then
    _evmfs="false"
  fi
fi
if [[ ! -v "_gles3" ]]; then
  _gles3="true"
fi
_pkg="mupen64plus-next"
_pkgname="libretro-${_pkg}"
_Pkg="mupen64plus-next"
pkgbase="${_pkgname}-bin"
pkgname=(
  "${_pkgname}-gles2-bin"
)
if [[ "${_gles3}" == "true" ]]; then
  pkgname+=(
    "${_pkgname}-gles3-bin"
  )
fi
pkgver="0.139"
pkgrel=1
_pkgdesc=(
  "RetroArch backend for"
  "the Mupen64Plus Next"
  "Nintendo 64 emulator."
)
pkgdesc="${_pkgdesc[*]}"
arch=(
  'arm'
  'armv7l'
)
_http="https://github.com"
_ns="libretro"
url="${_http}/${_ns}/${_pkg}-libretro"
license=(
  'GPL3'
)
depends=(
  'retroarch'
)
if [[ "${_os}" != "GNU/Linux" ]] && \
   [[ "${_os}" == "Android" ]]; then
  depends+=(
    'inteppacman'
  )
fi
optdepends=(
)
if [[ "${_os}" != "GNU/Linux" ]] && \
   [[ "${_os}" == "Android" ]]; then
  optdepends+=(
  )
fi
makedepends=(
  'coreutils'
)
if [[ "${_evmfs}" == "true" ]]; then
  makedepends+=(
    'evmfs'
  )
fi
checkdepends=(
)
provides=(
  "${_pkgname}=${pkgver}"
)
conflicts=(
  "${_pkgname}"
)
source=()
sha256sums=()
_lib_gles2="mupen64plus_next_gles2_libretro_android.so"
_lib_gles3="mupen64plus_next_gles3_libretro_android.so"
# This file has been published onto Ethereum Holesky testnet.
# That network may disappear sooner or later, so you'll have to crowd-publish it
# onto mainnets download after download on the mainnets when crowd-publishing
# will be ready.
# _evmfs_network="17000"
_evmfs_network="7001"
_evmfs_sig_network="100"
# _evmfs_address="0x151920938488F193735e83e052368cD41F9d9362"
_evmfs_address="0x7D55E8B250DC2393255d62db57C4C8bF7BCf23ec"
_evmfs_sig_address="0x69470b18f8b8b5f92b48f6199dcb147b4be96571"
# The kid
_evmfs_ns="0x926acb6aA4790ff678848A9F1C59E578B148C786"
# Dvorak
_evmfs_sig_ns="0x87003Bd6C074C713783df04f36517451fF34CBEf"
_lib_gles2_sum="4ee8f24e075cbfa87cd7b76519bb3522c55633f51291933701b2ec5758944344"
_lib_gles3_sum="fc0cb49c5c0e07622a6f061c095dc3c4c95596904312796568c4a8def11fc1c6"
_lib_gles3_sig_sum="aa6c5dbdb0c1b6ee89903347f8c44a8cf87a64a522ed2c7bf5f901a17fe683ef"
_lib_gles2_sig_sum="e2a7588e296a6477e37e7e07b0641cb38301e400d028d661a31d265f5cc4040c"
_http="https://github.com"
_ns="6xrS42VaMBgMbWRPAiVP"
_url="${_http}/${_ns}/${pkgname}"
_commit="171f10df1c118cac425e136727c6464c1b20046f"
_evmfs_lib_gles2_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_lib_gles2_sum}"
_evmfs_lib_gles2_sig_uri="evmfs://${_evmfs_sig_network}/${_evmfs_sig_address}/${_evmfs_sig_ns}/${_lib_gles2_sig_sum}"
_evmfs_lib_gles3_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_lib_gles3_sum}"
_evmfs_lib_gles3_sig_uri="evmfs://${_evmfs_sig_network}/${_evmfs_sig_address}/${_evmfs_sig_ns}/${_lib_gles3_sig_sum}"
source=()
sha256sums=()
if [[ "${_evmfs}" == "true" ]]; then
  _lib_gles2_src="${_lib_gles2}.tar.xz::${_evmfs_lib_gles2_uri}"
  _lib_gles2_sig_src="${_lib_gles2}.tar.xz.sig::${_evmfs_lib_gles2_sig_uri}"
  _lib_gles3_src="${_lib_gles3}.tar.xz::${_evmfs_lib_gles3_uri}"
  _lib_gles3_sig_src="${_lib_gles3}.tar.xz.sig::${_evmfs_lib_gles3_sig_uri}"
  if [[ "${_gles3}" == "true" ]]; then
    source+=(
      "${_lib_gles3_src}"
      "${_lib_gles3_sig_src}"
    )
    sha256sums+=(
      "${_lib_gles3_sum}"
      "${_lib_gles3_sig_sum}"
    )
  fi
elif [[ "${_evmfs}" == "false" ]]; then
  _lib_gles2_src="${_lib_gles2}.tar.xz::${_url}/raw/${_commit}/${_lib_gles2}.arm.tar.xz"
  _lib_gles2_sig_src="${_lib_gles2}.tar.xz.sig::${_url}/raw/${_commit}/${_lib_gles2}.arm.tar.xz.sig"
  _lib_gles3_src="${_lib_gles3}.tar.xz::${_url}/raw/${_commit}/${_lib_gles3}.arm.tar.xz"
  _lib_gles3_sig_src="${_lib_gles3}.tar.xz.sig::${_url}/raw/${_commit}/${_lib_gles3}.arm.tar.xz.sig"
fi
if [[ "${_gles3}" == "true" ]]; then
  source+=(
    "${_lib_gles3_src}"
    "${_lib_gles3_sig_src}"
  )
  sha256sums+=(
    "${_lib_gles3_sum}"
    "${_lib_gles3_sig_sum}"
  )
fi
source+=(
  "${_lib_gles2_src}"
  "${_lib_gles2_sig_src}"
)
sha256sums+=(
  "${_lib_gles2_sum}"
  "${_lib_gles2_sig_sum}"
)
validgpgkeys=(
  # Truocolo
  #   <truocolo@aol.com>
  '97E989E6CF1D2C7F7A41FF9F95684DBE23D6A3E9'
  # Truocolo
  #   <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
  'F690CBC17BD1F53557290AF51FC17D540D0ADEED'
  # Pellegrino Prevete (dvorak)
  #   <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>
  '12D8E3D7888F741E89F86EE0FEC8567A644F1D16'
)

package_libretro-mupen64plus-next-gles2-bin() {
  local \
    _dest_dir
  provides+=(
    "${_pkgname}-gles2=${pkgver}"
  )
  conflicts+=(
    "${_pkgname}-gles2"
  )
  _dest_dir="/data/data/com.retroarch/cores"
  install \
    -dm755 \
    "${pkgdir}${_dest_dir}"
  install \
    -Dm644 \
    "${srcdir}/${_lib_gles2}" \
    "${pkgdir}/${_dest_dir}/${_lib_gles2}"
}

package_libretro-mupen64plus-next-gles3-bin() {
  local \
    _dest_dir
  provides+=(
    "${_pkgname}-gles3=${pkgver}"
  )
  conflicts+=(
    "${_pkgname}-gles3"
  )
  _dest_dir="/data/data/com.retroarch/cores"
  install \
    -dm755 \
    "${pkgdir}${_dest_dir}"
  install \
    -Dm644 \
    "${srcdir}/${_lib_gles2}" \
    "${pkgdir}/${_dest_dir}/${_lib_gles3}"
}


# vim: ft=sh syn=sh et
