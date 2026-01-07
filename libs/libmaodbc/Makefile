# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libmaodbc
PKG_VERSION:=3.2.8
LIB_VERSION:=3.4.5
PKG_RELEASE:=1

#PKG_SOURCE:=mariadb-connector-odbc-$(PKG_VERSION)-src.tar.gz
#PKG_SOURCE_URL := \
#	https://mirror.netcologne.de/mariadb/connector-odbc-$(PKG_VERSION) \
#	https://mirror.lstn.net/mariadb/connector-odbc-$(PKG_VERSION) \
#	https://ftp.yz.yamagata-u.ac.jp/pub/dbms/mariadb/connector-odbc-$(PKG_VERSION) \
#	https://downloads.mariadb.org/interstitial/connector-odbc-$(PKG_VERSION)
#PKG_HASH:=9968979aae46a1750452eb934558af81c6eda957eaee00f7ec72b24ee8ead547
#PKG_BUILD_DIR:=$(BUILD_DIR)/mariadb-connector-odbc-$(PKG_VERSION)-src

PKG_SOURCE_URL=https://github.com/mariadb-corporation/mariadb-connector-odbc.git
PKG_MIRROR_HASH:=b23c0a4804a1bccb3988015415efaab1ec66e8567fd72b3c96ea84f56980a88d
PKG_SOURCE_PROTO:=git
PKG_SOURCE_DATE:=2025-12-17
PKG_SOURCE_VERSION:=84f6fd15c2d8f39d0b1725dc02da488019eae10f

PKG_MAINTAINER:=
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_PARALLEL:=1
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

# Pass CPPFLAGS in the CFLAGS as otherwise the build system will
# ignore them.
TARGET_CFLAGS+=$(TARGET_CPPFLAGS)

# We won't need unit tests
CMAKE_OPTIONS += -DCONC_WITH_UNIT_TESTS=Off

# Make it explicit that we are cross-compiling
CMAKE_OPTIONS += -DCMAKE_CROSSCOMPILING=1

CMAKE_OPTIONS += -DCONC_WITH_MSI=OFF \
	-DDEFAULT_CHARSET=utf8 \
	-DDEFAULT_COLLATION=utf8_general_ci \
	-DINSTALL_INCLUDEDIR=include/mysql \
	-DINSTALL_LIBDIR=lib \
	-DINSTALL_PLUGINDIR=lib/mariadb/plugin \
	-DMARIADB_UNIX_ADDR=$(MARIADB_SOCKET) \
	-DWITH_EXTERNAL_ZLIB=YES \
	-DWITH_MYSQLCOMPAT=ON \
	-DWITH_SSL=OPENSSL \
	-DCMAKE_BUILD_TYPE=RELEASE

define Package/libmaodbc
  SUBMENU:=Database
  URL:=https://mariadb.com/kb/en/mariadb-connector-odbc/
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=MariaDB Connector/ODBC
  DEPENDS:=+unixodbc +libmariadb +libstdcpp
endef

define Package/libmaodbc/description
	MariaDB Connector/ODBC is a database driver that uses the industry standard Open Database Connectivity (ODBC) API
endef

#define Build/Prepare
#	$(call Build/Prepare/Default)
#	mkdir $(PKG_BUILD_DIR)/libmariadb
#	tar xf $(DL_DIR)/mariadb-connector-c-$(LIB_VERSION)-src.tar.gz --strip-components=1 -C $(PKG_BUILD_DIR)/libmariadb
#endef

define Package/libmaodbc/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmaodbc.so $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/etc/odbcinst.ini.d
	echo "[MySQL]" > $(1)/etc/odbcinst.ini.d/libmaodbc.ini
	echo "Description = ODBC Driver for MySQL" >> $(1)/etc/odbcinst.ini.d/libmaodbc.ini
	echo "Driver = /usr/lib/libmaodbc.so" >> $(1)/etc/odbcinst.ini.d/libmaodbc.ini
endef

$(eval $(call BuildPackage,libmaodbc))
