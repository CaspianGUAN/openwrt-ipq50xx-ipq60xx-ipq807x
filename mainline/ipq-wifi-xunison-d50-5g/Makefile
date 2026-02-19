include $(TOPDIR)/rules.mk

PKG_NAME:=ipq-wifi-xunison_d50-5g
PKG_RELEASE:=1
PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/ipq-wifi-xunison_d50-5g
  SUBMENU:=ath11k Board-Specific Overrides
  SECTION:=firmware
  CATEGORY:=Firmware
  DEPENDS:=@TARGET_qualcommax_ipq50xx_DEVICE_xunison_d50-5g
  TITLE:=Xunison D50-5G WiFi calibration data (BDF)
endef

define Package/ipq-wifi-xunison_d50-5g/description
  WiFi Board Data Files (BDF) for the Xunison D50-5G.
  Provides calibration data for:
  - IPQ5018 internal 2.4G/5G radio
  - QCN9074 PCIe 5G module
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
endef

define Package/ipq-wifi-xunison_d50-5g/install
	$(INSTALL_DIR) $(1)/lib/firmware/ath11k/IPQ5018/hw1.0/
	$(INSTALL_DIR) $(1)/lib/firmware/ath11k/QCN9074/hw1.0/
	$(INSTALL_DATA) ./board-xunison-d50-5g.bin.IPQ5018 \
		$(1)/lib/firmware/ath11k/IPQ5018/hw1.0/board.bin
	$(INSTALL_DATA) ./board-xunison-d50-5g.bin.QCN9074 \
		$(1)/lib/firmware/ath11k/QCN9074/hw1.0/board.bin
endef

$(eval $(call BuildPackage,ipq-wifi-xunison_d50-5g))
