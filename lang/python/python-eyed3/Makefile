#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-eyed3
PKG_VERSION:=0.9.9
PKG_RELEASE:=1

#PYPI_NAME:=eyeD3
#PYTHON3_PKG_WHEEL_NAME:=eyed3
PKG_HASH:=a8affaae19384aca66f6efef3babd705042a76e546f08e886f5f28691ac62a3b

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=GPL3
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-eyed3
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python tool for working with audio files
  URL:=https://eyed3.readthedocs.io/
  DEPENDS:= \
	+python3 \
	+python3-filetype \
	+python3-deprecation \
	+python3-yaml
endef

define Package/python3-eyed3/description
  Python tool for working with audio files
endef

$(eval $(call Py3Package,python3-eyed3))
$(eval $(call BuildPackage,python3-eyed3))
