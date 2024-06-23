PKG_NAME = smartmontools
PKG_VERS = 7.4
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://downloads.sourceforge.net/project/smartmontools/smartmontools/$(PKG_VERS)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = https://www.smartmontools.org/
COMMENT  = Control and Monitor Utility for SMART Disks.
LICENSE  = GPLv2+

GNU_CONFIGURE = 1

CONFIGURE_ARGS  = --without-exampledir
CONFIGURE_ARGS += --disable-sample
CONFIGURE_ARGS += --prefix=$(INSTALL_PREFIX)
CONFIGURE_ARGS += --sbindir=$(INSTALL_PREFIX)/bin
CONFIGURE_ARGS += --with-drivedbdir=$(INSTALL_PREFIX)/share
CONFIGURE_ARGS += --without-initscriptdir
CONFIGURE_ARGS += --without-selinux
CONFIGURE_ARGS += --without-smartdscriptdir

COMPILE_MAKE_OPTIONS += CC="$(TC_PATH)$(TC_PREFIX)gcc"
COMPILE_MAKE_OPTIONS += CXX="$(TC_PATH)$(TC_PREFIX)g++"

include ../../mk/spksrc.cross-cc.mk
