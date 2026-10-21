#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-aiodns
PKG_VERSION:=4.0.4
PKG_RELEASE:=1

PYPI_NAME:=aiodns
PKG_HASH:=cb10e0c0d2591636716ad2fe402e977c16d71bdaf76bb8cb49e8a6633596f736

PKG_MAINTAINER:=Josef Schlehofer <pepe.schlehofer@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_CPE_ID:=cpe:/a:aiodns:aiodns

# pyproject build-system.requires lists pycares. OpenWrt's python-pycares
# package is target-only, so there is no python-pycares/host to depend on.
PKG_BUILD_DEPENDS:=python-setuptools/host

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
