#
# Copyright (C) 2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=webui-aria2
PKG_SOURCE_DATE:=2017-04-02
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ziahamza/webui-aria2
PKG_SOURCE_VERSION:=d2a662849a792bb8d7b83519bac1eeee0fcec4e9

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=Hsing-Wang Liao <kuoruan@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/webui-aria2
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Download Manager
  DEPENDS:=
  TITLE:=An interface to interact with aria2
  URL:=https://github.com/ziahamza/webui-aria2
  PKGARCH:=all
endef

define Package/webui-aria2/description
	The aim for this project is to create the worlds best and hottest interface to interact with aria2. Very simple to use.
endef

define Build/Compile
endef

define Package/webui-aria2/install
	$(INSTALL_DIR) \
		$(1)/www/webui-aria2 \
		$(1)/www/webui-aria2/flags/4x3

	$(CP) \
		$(PKG_BUILD_DIR)/{css,fonts,js} \
		$(PKG_BUILD_DIR)/{LICENSE,configuration.js,favicon.ico,index.html} \
		$(1)/www/webui-aria2

	$(CP) \
		$(PKG_BUILD_DIR)/flags/4x3/{cn,de,es,fr,it,nl,pl,ru,th,tr,tw,us}.svg \
		$(1)/www/webui-aria2/flags/4x3
endef

$(eval $(call BuildPackage,webui-aria2))
