#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-aiodns
PKG_VERSION:=3.6.1
PKG_RELEASE:=1

PYPI_NAME:=aiodns
PKG_HASH:=b0e9ce98718a5b8f7ca8cd16fc393163374bc2412236b91f6c851d066e3324b6

PKG_MAINTAINER:=Josef Schlehofer <pepe.schlehofer@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.txt
PKG_CPE_ID:=cpe:/a:aiodns:aiodns

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-aiodns
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Simple DNS resolver for asyncio
  URL:=https://github.com/aio-libs/aiodns
  DEPENDS:= \
	+python3 \
	+python3-pycares
endef

define Package/python3-aiodns/description
  Simple DNS resolver for asyncio
endef

$(eval $(call Py3Package,python3-aiodns))
$(eval $(call BuildPackage,python3-aiodns))
