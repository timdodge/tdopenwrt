#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-libscrc
PKG_VERSION:=1.8.1
PKG_RELEASE:=1

PYPI_NAME:=libscrc
PKG_HASH:=d7ba6bf23cfdeb3b729d0ad3795f6c6f97d8ea4155252e3ca9f14758702ba7c8

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=GPL3
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-libscrc
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Library for calculating CRCs
  URL:=https://github.com/hex-in/libscrc
  DEPENDS:= \
	+python3
endef

define Package/python3-libscrc/description
  Library for calculating CRCs
endef

$(eval $(call Py3Package,python3-libscrc))
$(eval $(call BuildPackage,python3-libscrc))
