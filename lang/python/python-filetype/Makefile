#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-filetype
PKG_VERSION:=1.2.0
PKG_RELEASE:=1

PYPI_NAME:=filetype
PKG_HASH:=66b56cd6474bf41d8c54660347d37afcc3f7d1970648de365c102ef77548aadb

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=GPL3
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-filetype
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Infer file type and MIME type of a file or buffer
  URL:=https://github.com/h2non/filetype.py
  DEPENDS:= \
	+python3
endef

define Package/python3-filetype/description
  Infer file type and MIME type of a file or buffer
endef

$(eval $(call Py3Package,python3-filetype))
$(eval $(call BuildPackage,python3-filetype))
