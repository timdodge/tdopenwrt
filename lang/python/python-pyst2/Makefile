#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-pyst2
PKG_VERSION:=0.5.1
PKG_RELEASE:=1

PYPI_NAME:=pyst2
PKG_HASH:=07e8f4154b18fc2d11c2873a426100685fc4483da9b29db2b5f937cacf1b81cf

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=LGPL
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-pyst2
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A Python Interface to Asterisk
  URL:=https://github.com/jfernandz/pyst2
  DEPENDS:= \
	+python3 \
	+python3-six
endef

define Package/python3-pyst2/description
  A Python Interface to Asterisk
endef

$(eval $(call Py3Package,python3-pyst2))
$(eval $(call BuildPackage,python3-pyst2))
