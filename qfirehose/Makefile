#
# Copyright (C) 2011-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=qfirehose
LUCI_TITLE:=Quectel flash utility
PKG_VERSION:=1.4.21
PKG_RELEASE:=1
PKG_LICENSE_FILES:=NOTICE
PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/qfirehose
  SECTION:=utils
  TITLE:=Quectel flash utility
endef

define Package/qfirehose/description
 Quectel FireHose
endef

define Build/Compile
	$(MAKE) -C $(PKG_BUILD_DIR) \
		CC="$(TARGET_CC)" \
		CFLAGS="$(TARGET_CFLAGS) -Wall"
endef

define Package/qfirehose/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/qfirehose $(1)/usr/bin/QFirehose
endef

$(eval $(call BuildPackage,qfirehose))
