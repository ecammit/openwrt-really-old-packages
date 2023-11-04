include $(TOPDIR)/rules.mk

PKG_NAME:=python-orjson
PKG_VERSION:=3.9.10
PKG_RELEASE:=1

PYPI_NAME:=orjson
PKG_HASH:=9ebbdbd6a046c304b1845e96fbcc5559cd296b4dfd3ad2509e33c4d9ce07d6a1

PKG_MAINTAINER:=Timothy Ace <ecammit@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-maturin/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/host-build.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-host-build.mk

define Package/python3-orjson
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Fast, correct Python JSON library supporting dataclasses, datetimes, and numpy
  URL:=https://github.com/ijl/orjson
  DEPENDS:= \
	+python3-light \
	+python3-dateutil \
	+python3-numpy \
	+python3-uuid
endef

define Package/python3-orjson/description
  Fast, correct Python JSON library supporting dataclasses, datetimes, and numpy
endef

$(eval $(call Py3Package,python3-orjson))
$(eval $(call BuildPackage,python3-orjson))
$(eval $(call BuildPackage,python3-orjson-src))
