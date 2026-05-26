ccflags-y += -I$(srctree)/include/drm

ccflags-y += -I$(srctree)/techpack/display/msm
ccflags-y += -I$(srctree)/techpack/display/msm/sde
ccflags-y += -I$(srctree)/techpack/display/msm/dsi
ccflags-y += -I$(srctree)/techpack/display/msm/dp
ccflags-y += -I$(srctree)/techpack/display/rotator

ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/main
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/vfps
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/fbcn
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/sben
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/triton
ccflags-y += -I$(srctree)/drivers/soc/qcom/lge/power/dd
		  
obj-$(CONFIG_MACH_LGE) += devices_lge.o
obj-$(CONFIG_LGE_BOOTLOADER_LOG) += lge_bootloader_log.o
obj-$(CONFIG_LGE_BOOTLOADER_TIME_CHECKER) += lge_bootloader_time_checker.o
obj-$(CONFIG_LGE_HANDLE_PANIC) += lge_handle_panic.o
obj-$(CONFIG_LGE_PM) += lge_gpio_debug.o
obj-$(CONFIG_LGE_PM) += lge_pon_backup.o
obj-$(CONFIG_LGE_QSDL_SUPPORT) += lge_qsdl.o
obj-$(CONFIG_LGE_QFPROM_INTERFACE) += lge_qfprom_access.o
obj-$(CONFIG_LGE_PM) += lge_monitor_thermal.o
obj-$(CONFIG_LGE_PM_SMPL_COUNTER) += lge_smpl_count.o
obj-$(CONFIG_LGE_PM_PRM) += power/main/lge_prm.o
obj-$(CONFIG_LGE_PM_PRM) += power/vfps/lge_vfps.o
obj-$(CONFIG_LGE_PM_PRM) += power/sben/lge_sben.o
obj-$(CONFIG_LGE_PM_PRM) += power/fbcn/lge_fbcn.o
obj-$(CONFIG_LGE_PM_PRM) += power/fbcn/lge_intm.o
obj-$(CONFIG_LGE_PM_PRM) += power/triton/lge_triton.o
obj-$(CONFIG_LGE_PM) += power/lrmc/lge_regulator_mode_change.o
obj-$(CONFIG_LGE_PM_PRM) += power/dd/lge_dd.o
obj-$(CONFIG_LGE_MME_BUS) += lge_mme_bus.o
obj-$(CONFIG_LGE_MME_DRV) += wmc_drv.o
wmc_drv-$(CONFIG_LGE_MME_DRV) += lge_mme_drv.o
