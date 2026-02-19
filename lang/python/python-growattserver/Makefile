#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-growattserver
PKG_VERSION:=1.9.0
PKG_RELEASE:=1


PYPI_NAME:=growattserver
#PYTHON3_PKG_WHEEL_NAME:=growattserver
PKG_HASH:=1af610b21f7d7b5b94fdfbf17a581493efed8bf00f3ebf14b2e3c08f0b6c3998

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-growattserver
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Package to retrieve PV information from the growatt server.
  URL:=https://github.com/indykoning/PyPi_GrowattServer
  DEPENDS:= \
	+python3 \
	+python3-requests
endef

define Package/python3-growattserver/description
  Package to retrieve PV information from the growatt server.
endef

$(eval $(call Py3Package,python3-growattserver))
$(eval $(call BuildPackage,python3-growattserver))
