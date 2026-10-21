#
# Copyright (C) 2008-2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=whisper.cpp
PKG_VERSION:=1.9.5
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/ggml-org/$(PKG_NAME)/archive/refs/tags/v$(PKG_VERSION).tar.gz?
PKG_HASH:=ff1a9053feb509ff9d7729703355541ae9690073a6b1c40eb692c962e0dc1720

PKG_MAINTAINER:=Tim Dodge <tim@dodge.me.uk>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

CMAKE_OPTIONS += \
  -DWHISPER_BUILD_IS_DEV=OFF \
  -DWHISPER_COMMON_FFMPEG=yes

define Package/whisper.cpp
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=+libstdcpp +libffmpeg-full
  TITLE:=Whisper automatic speech recognition model
  URL:=https://github.com/ggml-org/whisper.cpp
endef

define Package/whisper.cpp/install
	$(INSTALL_DIR) $(1)/usr/bin $(1)/usr/lib
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/whisper-cli $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/models/download-ggml-model.sh $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/*.so* $(1)/usr/lib
endef

$(eval $(call BuildPackage,whisper.cpp))
