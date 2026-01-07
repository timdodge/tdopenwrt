#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-deprecation
PKG_VERSION:=2.1.0
PKG_RELEASE:=1

PYPI_NAME:=deprecation
PKG_HASH:=72b3bde64e5d778694b0cf68178aed03d15e15477116add3fb773e581f9518ff

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-deprecation
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Provides a deprecated decorator
  URL:=http://deprecation.readthedocs.io/
  DEPENDS:= \
	+python3 \
	+python3-packaging
endef

define Package/python3-deprecation/description
  Provides a deprecated decorator
endef

$(eval $(call Py3Package,python3-deprecation))
$(eval $(call BuildPackage,python3-deprecation))
