#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-propcache
PKG_VERSION:=0.5.4
PKG_RELEASE:=1

PYPI_NAME:=propcache
PKG_HASH:=ff6b113f50bc066a698db5d944d2c6dc7507168dd3341e255a8892fd0715a558

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE NOTICE

PKG_BUILD_DEPENDS:=python-setuptools/host python-expandvars/host python-cython/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-propcache
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Accelerated property cache
  URL:=https://github.com/aio-libs/propcache
  DEPENDS:=+python3-light
endef

define Package/python3-propcache/description
  Fast implementation of cached properties.
endef

$(eval $(call Py3Package,python3-propcache))
$(eval $(call BuildPackage,python3-propcache))
