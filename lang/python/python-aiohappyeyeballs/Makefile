#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-aiohappyeyeballs
PKG_VERSION:=2.7.1
PKG_RELEASE:=1

PYPI_NAME:=aiohappyeyeballs
PKG_HASH:=065665c041c42a5938ed220bdcd7230f22527fbec085e1853d2402c8a3615d9d

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=PSF-2.0
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-poetry-core/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-aiohappyeyeballs
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Happy Eyeballs for asyncio
  URL:=https://github.com/aio-libs/aiohappyeyeballs
  DEPENDS:=+python3-light
endef

define Package/python3-aiohappyeyeballs/description
  Happy Eyeballs (RFC 8305) for asyncio when addrinfo is already resolved.
endef

$(eval $(call Py3Package,python3-aiohappyeyeballs))
$(eval $(call BuildPackage,python3-aiohappyeyeballs))
