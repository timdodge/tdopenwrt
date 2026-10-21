#
# Copyright (C) 2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-forecast-solar
PKG_VERSION:=5.0.1
PKG_RELEASE:=1

PYPI_NAME:=forecast_solar
PKG_HASH:=cc84a042a4b1076bc9dc25932472d267f72cdca70a4a8b3c74ac6672644d1a66

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>

PKG_BUILD_DEPENDS:=python-poetry-core/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-forecast-solar
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Fetch Solarpanel forecast information
  URL:=https://github.com/home-assistant-libs/forecast_solar
  DEPENDS:=+python3 \
  +python3-aiohttp \
  +python3-yarl
endef

define Package/python-dns/description
Python API fetching Solarpanels forecast information.
With this python library you can request data from forecast.solar and 
see what your solar panels may produce in the coming days.
endef

$(eval $(call Py3Package,python3-forecast-solar))
$(eval $(call BuildPackage,python3-forecast-solar))
