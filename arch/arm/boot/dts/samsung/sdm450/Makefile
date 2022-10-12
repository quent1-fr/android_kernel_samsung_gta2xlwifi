# Samsung SDM450 Project

dtb-$(CONFIG_MACH_GTA2XLLTE_EUR_OPEN) += sdm450-sec-gta2xllte_eur_open-r00.dtb \
					sdm450-sec-gta2xllte_eur_open-r01.dtb \
					sdm450-sec-gta2xllte_eur_open-r02.dtb \
					sdm450-sec-gta2xllte_eur_open-r03.dtb \
					sdm450-sec-gta2xllte_eur_open-r04.dtb \
					sdm450-sec-gta2xllte_eur_open-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLLTE_CHN_OPEN) += sdm450-sec-gta2xllte_chn_open-r00.dtb \
					sdm450-sec-gta2xllte_chn_open-r01.dtb \
					sdm450-sec-gta2xllte_chn_open-r02.dtb \
					sdm450-sec-gta2xllte_chn_open-r03.dtb \
					sdm450-sec-gta2xllte_chn_open-r04.dtb \
					sdm450-sec-gta2xllte_chn_open-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLLTE_USA_SPR) += sdm450-sec-gta2xllte_usa_spr-r00.dtb \
					sdm450-sec-gta2xllte_usa_spr-r01.dtb \
					sdm450-sec-gta2xllte_usa_spr-r02.dtb \
					sdm450-sec-gta2xllte_usa_spr-r03.dtb \
					sdm450-sec-gta2xllte_usa_spr-r04.dtb \
					sdm450-sec-gta2xllte_usa_spr-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLLTE_USA_VZW) += sdm450-sec-gta2xllte_usa_vzw-r00.dtb \
					sdm450-sec-gta2xllte_usa_vzw-r01.dtb \
					sdm450-sec-gta2xllte_usa_vzw-r02.dtb \
					sdm450-sec-gta2xllte_usa_vzw-r03.dtb \
					sdm450-sec-gta2xllte_usa_vzw-r04.dtb \
					sdm450-sec-gta2xllte_usa_vzw-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLLTE_CAN_SINGLE) += sdm450-sec-gta2xllte_can_single-r00.dtb \
					sdm450-sec-gta2xllte_can_single-r01.dtb \
					sdm450-sec-gta2xllte_can_single-r02.dtb \
					sdm450-sec-gta2xllte_can_single-r03.dtb \
					sdm450-sec-gta2xllte_can_single-r04.dtb \
					sdm450-sec-gta2xllte_can_single-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLLTE_MEA_OPEN) += sdm450-sec-gta2xllte_mea_open-r00.dtb \
					sdm450-sec-gta2xllte_mea_open-r01.dtb \
					sdm450-sec-gta2xllte_mea_open-r02.dtb \
					sdm450-sec-gta2xllte_mea_open-r03.dtb \
					sdm450-sec-gta2xllte_mea_open-r04.dtb \
					sdm450-sec-gta2xllte_mea_open-r05.dtb
					
dtb-$(CONFIG_MACH_GTA2XLLTE_MEA_TUR) += sdm450-sec-gta2xllte_mea_tur-r00.dtb \
					sdm450-sec-gta2xllte_mea_tur-r01.dtb \
					sdm450-sec-gta2xllte_mea_tur-r02.dtb \
					sdm450-sec-gta2xllte_mea_tur-r03.dtb \
					sdm450-sec-gta2xllte_mea_tur-r04.dtb \
					sdm450-sec-gta2xllte_mea_tur-r05.dtb

dtb-$(CONFIG_MACH_GTA2XLWIFI_EUR_OPEN) += sdm450-sec-gta2xlwifi_eur_open-r02.dtb \
					sda450-sec-gta2xlwifi_eur_open-r02.dtb \
					sda450-sec-gta2xlwifi_eur_open-r03.dtb \
					sda450-sec-gta2xlwifi_eur_open-r04.dtb \
					sda450-sec-gta2xlwifi_eur_open-r05.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(dtb-y))
endif
clean-files := *.dtb *.reserve.dts
