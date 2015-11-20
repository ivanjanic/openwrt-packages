#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=gptfdisk
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=http://www.rodsbooks.com/gdisk/
PKG_MD5SUM:=d7f3d306b083123bcc6f5941efade586

include $(INCLUDE_DIR)/package.mk

define Package/gptfdisk
  SECTION:=utils
  CATEGORY:=Utilities
  SUBMENU:=disc
  TITLE:=Partition table manipulation utility with GPT support
  URL:=http://www.rodsbooks.com/gdisk
  DEPENDS:=+libncursesw +libuuid +libstdcpp +libpopt
endef

define Package/gptfdisk/description
 Partition table manipulation utility with GPT support
endef

define Package/gptfdisk/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/cgdisk $(1)/usr/sbin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fixparts $(1)/usr/sbin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/gdisk $(1)/usr/sbin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/sgdisk $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,gptfdisk))
