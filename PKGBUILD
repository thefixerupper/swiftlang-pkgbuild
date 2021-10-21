# A package build script for Swift adapted for Arch Linux from
# https://github.com/apple/swift-installer-scripts
#
# To get the latest version, visit
# https://github.com/thefixerupper/swiftlang-pkgbuild

pkgname='swiftlang'
pkgver='5.5.0'
pkgrel='1'
pkgdesc='The Swift programming language'

url='https://swift.org/'

_swift_version='5.5-RELEASE'
_swift_argument_parser_version='0.4.3'
_icu_version='65-1'
_yams_version='4.0.2'
_swift_crypto_version='1.1.5'

arch=('x86_64')
license=('apache2')

depends=(
    'binutils'
    'gcc'
    'gcc-libs' # libstdc++
    'git'
    'glibc'
    'icu' # libicu
    'libbsd'
    'libedit'
    'pkgconf'
    'python'
    'sqlite'
    'zlib'
)

makedepends=(
    'autoconf'
    'clang'
    'cmake'
    'curl' # libcurl
    'diffutils'
    'gcc-libs' # libstdc++
    'git'
    'glibc'
    'libbsd'
    'libedit'
    'icu' # libicu
    'libtool'
    'libxml2'
    'make'
    'ninja'
    'ncurses'
    'patch'
    'pcre'
    'python'
    'python-six'
    'python-pexpect'
    'python'
    'sqlite'
    'swig'
    'rsync'
    'tar'
    'util-linux-libs' # libuuid
    'which'
)

source=(
    "swift.tar.gz::https://github.com/apple/swift/archive/swift-${_swift_version}.tar.gz"
    "corelibs-libdispatch.tar.gz::https://github.com/apple/swift-corelibs-libdispatch/archive/swift-${_swift_version}.tar.gz"
    "corelibs-foundation.tar.gz::https://github.com/apple/swift-corelibs-foundation/archive/swift-${_swift_version}.tar.gz"
    "swift-integration-tests.tar.gz::https://github.com/apple/swift-integration-tests/archive/swift-${_swift_version}.tar.gz"
    "corelibs-xctest.tar.gz::https://github.com/apple/swift-corelibs-xctest/archive/swift-${_swift_version}.tar.gz"
    "package-manager.tar.gz::https://github.com/apple/swift-package-manager/archive/swift-${_swift_version}.tar.gz"
    "llbuild.tar.gz::https://github.com/apple/swift-llbuild/archive/swift-${_swift_version}.tar.gz"
    "cmark.tar.gz::https://github.com/apple/swift-cmark/archive/swift-${_swift_version}.tar.gz"
    "swift-xcode-playground-support.tar.gz::https://github.com/apple/swift-xcode-playground-support/archive/swift-${_swift_version}.tar.gz"
    "sourcekit-lsp.tar.gz::https://github.com/apple/sourcekit-lsp/archive/swift-${_swift_version}.tar.gz"
    "indexstore-db.tar.gz::https://github.com/apple/indexstore-db/archive/swift-${_swift_version}.tar.gz"
    "llvm-project.tar.gz::https://github.com/apple/llvm-project/archive/swift-${_swift_version}.tar.gz"
    "swift-tools-support-core.tar.gz::https://github.com/apple/swift-tools-support-core/archive/swift-${_swift_version}.tar.gz"
    "swift-argument-parser.tar.gz::https://github.com/apple/swift-argument-parser/archive/${_swift_argument_parser_version}.tar.gz"
    "swift-driver.tar.gz::https://github.com/apple/swift-driver/archive/swift-${_swift_version}.tar.gz"
    "icu.tar.gz::https://github.com/unicode-org/icu/archive/release-${_icu_version}.tar.gz"
    "swift-syntax.tar.gz::https://github.com/apple/swift-syntax/archive/swift-${_swift_version}.tar.gz"
    "yams.tar.gz::https://github.com/jpsim/Yams/archive/${_yams_version}.tar.gz"
    "swift-crypto.tar.gz::https://github.com/apple/swift-crypto/archive/refs/tags/${_swift_crypto_version}.tar.gz"
    'swift.patch'
    'swift-corelibs-foundation.patch'
)

sha256sums=(
    '0f76c429e65f24d48a2a18b18e7b380a5c97be0d4370271ac3623e436332fd35'
    '5efdfa1d2897c598acea42fc00776477bb3713645686774f5ff0818b26649e62'
    '4d58bd3ed05f8b2bf836e4868034f01272dddbd3c0385ddc6f2afc93da033464'
    'bb1131f8b481c8b8b112ebe486db1525e1307b5d34e71201d2ce8c67be506f64'
    '4dd3a3096c51b52817b0876ce18ea921cb0f71adf1992019e984d0d45e49b840'
    '89b240810b1c2adb86ba83a70ec384b75608a737f9af09f469c8ca968a85a30e'
    '09e774c4a97bbb7473ab2b69ef2a547036660ce7d5d2c67802974de3e23381f8'
    '689865cafeb0bd7eb1297cdd8ba06c43d072af921d36bdbdf6dbe3817b3bb27f'
    'bcd54a3e5f496340b25c610381c3a9e8024f28572032444875d26a7a93630e33'
    '21bca4b8a84a4b687dc9ab1090fd3433915d7555445687ad82f1eaf3ec23c738'
    '191711ad5d7638091b8c813335a7831c7e549a82b3fd480e368ed8ad7801d62d'
    '87955764fb6cd83cb24e0421f249ce3fc817400edd3c0015eb840fe7fd7cf5e3'
    '4ae77edeb30a311d6d4bd5a4ed5ce7286d8fb3305d962a702a985297c82053d0'
    '9dfcb236f599e309e49af145610957648f8a59d9527b4202bc5bdda0068556d7'
    'e6c8ec5fc41f05ffd4c04b409278d0b4ec098402304b20d2997f06ea2ed2e4ed'
    'b3afd3093becc62e74220e7ac422f8a4f95328c3da85dfabd57ecd2b4c90455b'
    'd9362cee23bbeb5740b113dd47c74f55f690cc5805dd4e3076ca5d56d2eed74b'
    '8bbb28ef994f60afe54668093d652e4d40831c79885fa92b1c2cd0e17e26735a'
    '86d6c22c9f89394fd579e967b0d5d0b6ce33cdbf52ba70f82fa313baf70c759f'
    '8e02032abf07e010042a8a82aa13a02823dfc091c79cb42a2aedabeeff8165d7'
    '7508809f38acd6e4005fd778fb75d78ec0fcce3f2e7cdb0c6943fcae9dee3548'
)

options=(!strip)

prepare() {
    cd "${srcdir}"

    # The Swift build script requires directories to be named
    # in a specific way so renaming the source directories is
    # necessary
    mv swift-cmark-swift-${_swift_version} cmark
    mv swift-corelibs-foundation-swift-${_swift_version} swift-corelibs-foundation
    mv swift-corelibs-libdispatch-swift-${_swift_version} swift-corelibs-libdispatch
    mv swift-corelibs-xctest-swift-${_swift_version} swift-corelibs-xctest
    mv swift-integration-tests-swift-${_swift_version} swift-integration-tests
    mv swift-llbuild-swift-${_swift_version} llbuild
    mv swift-package-manager-swift-${_swift_version} swiftpm
    mv swift-swift-${_swift_version} swift
    mv swift-xcode-playground-support-swift-${_swift_version} swift-xcode-playground-support
    mv sourcekit-lsp-swift-${_swift_version} sourcekit-lsp
    mv indexstore-db-swift-${_swift_version} indexstore-db
    mv llvm-project-swift-${_swift_version} llvm-project
    mv swift-syntax-swift-${_swift_version} swift-syntax
    mv swift-tools-support-core-swift-${_swift_version} swift-tools-support-core
    mv swift-argument-parser-${_swift_argument_parser_version} swift-argument-parser
    mv swift-driver-swift-${_swift_version} swift-driver
    mv swift-crypto-${_swift_crypto_version} swift-crypto

    # ICU
    mv icu-release-${_icu_version} icu

    # Yams
    mv Yams-${_yams_version} yams

    # Distribution patches
    cd "${srcdir}/swift"
    patch -p1 -i "${srcdir}/swift.patch"


    cd "${srcdir}/swift-corelibs-foundation"
    patch -p1 -i "${srcdir}/swift-corelibs-foundation.patch"

    # More distribution patching
    cd "${srcdir}"
    find "${srcdir}/swift/stdlib/public/SwiftShims" -type f -print0 \
        | xargs -0 sed -i 's|/usr/include/x86_64-linux-gnu|/usr/include|g'
    find "${srcdir}/llvm-project/clang" -type f -print0 \
        | xargs -0 sed -i 's|/usr/include/x86_64-linux-gnu|/usr/include|g'
    find "${srcdir}/llvm-project/clang-tools-extra" -type f -print0 \
        | xargs -0 sed -i 's|/usr/include/x86_64-linux-gnu|/usr/include|g'
}

build() {
    unset CPPFLAGS

    cd "${srcdir}"
    mkdir -p destdir

    swift/utils/build-script --preset=buildbot_linux,no_test install_destdir=destdir
}

package() {
    mkdir -p "${pkgdir}/usr/lib/swift/"
    cp -r "${srcdir}/destdir/usr/"* "${pkgdir}/usr/lib/swift"
    mkdir -p "${pkgdir}/usr/bin"
    ln -fs "/usr/lib/swift/bin/swift" "${pkgdir}/usr/bin/swift"
    ln -fs "/usr/lib/swift/bin/swiftc" "${pkgdir}/usr/bin/swiftc"
    ln -fs "/usr/lib/swift/bin/sourcekit-lsp" "${pkgdir}/usr/bin/sourcekit-lsp"
    mkdir -p "${pkgdir}/usr/share/man/man1"
    cp "${srcdir}/destdir/usr/share/man/man1/swift.1" "${pkgdir}/usr/share/man/man1/swift.1"
}
