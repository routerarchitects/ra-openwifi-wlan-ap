include $(TOPDIR)/rules.mk

PKG_NAME:=ucentral-tools
PKG_RELEASE:=1

PKG_SOURCE_URL=https://github.com/routerarchitects/ucentral-tools.git
PKG_MIRROR_HASH:=6b69ac0378d879e1a78606bc837e8f8a3d6ba8a6c53817acbcce987a639ad04d
PKG_SOURCE_PROTO:=git
PKG_SOURCE_DATE:=2025-09-29
PKG_SOURCE_VERSION:=17bd7d5574a0f62b972c40898710f04509b7cf64
PKG_MAINTAINER:=John Crispin <john@phrozen.org>
PKG_LICENSE:=BSD-3-Clause

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/ucentral-tools
  SECTION:=ucentral
  CATEGORY:=uCentral
  TITLE:=ucentral tools collection
  DEPENDS:=+libubox +libcurl +libradcli +libopenssl
endef

define Package/ucentral-tools/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/{dhcpdiscover,dnsprobe,radiusprobe,ip-collide} $(1)/usr/sbin/
	$(CP) ./files/* $(1)
endef

$(eval $(call BuildPackage,ucentral-tools))
