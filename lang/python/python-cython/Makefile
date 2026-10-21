#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-cython
PKG_VERSION:=3.3.0
PKG_RELEASE:=1

PYPI_NAME:=Cython
PYPI_SOURCE_NAME:=cython
PKG_HASH:=eed0d93fbca7087f143b42c34b05a825849bdf17f101572c2105acfa49aa88b8

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE.txt

PKG_HOST_ONLY:=1
HOST_BUILD_DEPENDS:= \
	python3/host \
	python-build/host \
	python-installer/host \
	python-wheel/host \
	python-setuptools/host \
	python-packaging/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-host-build.mk

define Package/python3-cython
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Cython compiler for writing C extensions
  URL:=https://cython.org/
  DEPENDS:=+python3
  BUILDONLY:=1
endef

define Package/python3-cython/description
  Cython is a language for writing C extensions for Python.
endef

$(eval $(call Py3Package,python3-cython))
$(eval $(call BuildPackage,python3-cython))
$(eval $(call BuildPackage,python3-cython-src))
$(eval $(call HostBuild))
