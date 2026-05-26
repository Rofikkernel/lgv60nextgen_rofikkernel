#
# Makefile for ams TCS3407 device.
#

ifeq ($(CONFIG_SENSORS_TCS3407),y)

#
# Feature Options
#
subdir-ccflags-y 	:= -DCONFIG_AMS_OPTICAL_SENSOR_3407

# ifeq ($(CONFIG_TCS3407_AMS_DEBUG_LOG), y)
subdir-ccflags-y 	+= -DCONFIG_AMS_DEBUG_LOG
subdir-ccflags-y 	+= -DCONFIG_AMS_CORE_LOG
# endif

#ifeq ($(CONFIG_TCS3407_AMS_OPTICAL_SENSOR_ALS), y)
subdir-ccflags-y 	+= -DCONFIG_ALS_CAL_TARGET=300
subdir-ccflags-y 	+= -DCONFIG_AMS_ALS_CRGBW
subdir-ccflags-y 	+= -DCONFIG_AMS_OPTICAL_SENSOR_ALS
subdir-ccflags-y 	+= -DCONFIG_AMS_OPTICAL_SENSOR_ALS_CCB
subdir-ccflags-y 	+= -DCONFIG_AMS_OPTICAL_SENSOR_ALS_RGB
# endif

#subdir-ccflags-y 	+= -DALS_AUTOGAIN
#subdir-ccflags-y 	+= -DAMS_SW_FLICKER

subdir-ccflags-y 	+= -DAMS_BIN_2048_MODE1
#subdir-ccflags-y 	+= -DAMS_BIN_2048_MODE2
 

#
# Include Paths
#
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/osal_linux_input/include
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/tcs3407_dev_ctrl_block/include
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/dev_com_iface/include
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/algorithm_als/include
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/ccb_als/include
subdir-ccflags-y += -I$(srctree)/drivers/input/misc/tcs3407/ccb_irbeam/include

#
# Object Artifacts
#
#obj-$(CONFIG_SENSORS_TCS3407)	+= tcs3407drv.o
obj-y	:= tcs3407_module.o
obj-y	+= osal_linux_input/src/osal_linux_input.o
obj-y	+= osal_linux_input/src/osal_linux_input_als.o
obj-y	+= tcs3407_dev_ctrl_block/src/ams_device_control_block.o
obj-y	+= tcs3407_dev_ctrl_block/src/ams_device_control_block_init.o
obj-y	+= dev_com_iface/src/ams_device_com_interface.o

obj-y	+= ams_fft_2048.o
#obj-y	+= ams_fft.o


#ifeq ($(CONFIG_TCS3407_AMS_OPTICAL_SENSOR_ALS), y)
obj-y	+= algorithm_als/src/ams_als_API_config.o
obj-y	+= algorithm_als/src/ams_als_API_info.o
obj-y	+= algorithm_als/src/ams_als_API_init.o
obj-y	+= algorithm_als/src/ams_als_API_process.o
obj-y	+= algorithm_als/src/ams_als_API_result.o
obj-y	+= algorithm_als/src/ams_als_core.o
obj-y	+= ccb_als/src/core_control_block_als.o
obj-y	+= ccb_als/src/core_control_block_als_init.o
# endif



endif
