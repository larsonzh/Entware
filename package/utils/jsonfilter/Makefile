include $(TOPDIR)/rules.mk

PKG_NAME:=jsonfilter
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL=$(PROJECT_GIT)/project/jsonpath.git
PKG_SOURCE_DATE:=2024-01-23
PKG_SOURCE_VERSION:=594cfa86469c005972ba750614f5b3f1af84d0f6
PKG_MIRROR_HASH:=2f455f04fbfcdb4c81cccd23475b47395f847db44aa4bd9a1007b9aa0ab7fd19
CMAKE_INSTALL:=1

PKG_MAINTAINER:=Jo-Philipp Wich <jo@mein.io>
PKG_LICENSE:=ISC

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/jsonfilter
  SECTION:=base
  CATEGORY:=Base system
  DEPENDS:=+libubox +libjson-c
  TITLE:=OpenWrt JSON filter utility
  URL:=$(PKG_SOURCE_URL)
endef

define Package/jsonfilter/install
	$(INSTALL_DIR) $(1)/opt/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/opt/bin/jsonpath $(1)/opt/bin/jsonfilter
endef

$(eval $(call BuildPackage,jsonfilter))
