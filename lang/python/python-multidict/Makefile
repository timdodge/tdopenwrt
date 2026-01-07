#
# Copyright (C) 2019 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-multidict
PKG_VERSION:=6.7.0
PKG_RELEASE:=1

PYPI_NAME:=multidict
PKG_HASH:=c6e99d9a65ca282e578dfea819cfa9c0a62b2499d8677392e09feaf305e9e6f5

PKG_MAINTAINER:=Josef Schlehofer <pepe.schlehofer@gmail.com>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-multidict
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=multidict implementation
  URL:=https://github.com/aio-libs/multidict
  DEPENDS:=+python3-light
endef

define Package/python3-multidict/description
Multidict is dict-like collection of key-value pairs where key might be
occurred more than once in the container.
endef

$(eval $(call Py3Package,python3-multidict))
$(eval $(call BuildPackage,python3-multidict))
