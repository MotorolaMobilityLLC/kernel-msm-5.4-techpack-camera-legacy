# SPDX-License-Identifier: GPL-2.0-only

# auto-detect subdirs
ifneq ($(CONFIG_ARCH_QTI_VM), y)
ifeq ($(CONFIG_ARCH_KONA), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/konacamera.conf
endif

ifeq ($(CONFIG_ARCH_LITO), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/litocamera.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/bengalcamera.conf
endif

ifeq ($(CONFIG_ARCH_MONACO), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/monacocamera.conf
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/lahainacamera.conf
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/holicamera.conf
endif

ifeq ($(CONFIG_ARCH_BLAIR), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/blaircamera.conf
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/shimacamera.conf
endif

ifeq ($(CONFIG_ARCH_YUPIK), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/yupikcamera.conf
endif

ifeq ($(CONFIG_ARCH_SM6150), y)
include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/sm6150camera.conf
endif

ifeq ($(CONFIG_ARCH_KONA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/konacameraconf.h
endif

ifeq ($(CONFIG_ARCH_LITO), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/litocameraconf.h
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/bengalcameraconf.h
endif

ifeq ($(CONFIG_ARCH_MONACO), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/monacocameraconf.h
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/lahainacameraconf.h
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/holicameraconf.h
endif

ifeq ($(CONFIG_ARCH_BLAIR), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/blaircameraconf.h
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/shimacameraconf.h
endif

ifeq ($(CONFIG_ARCH_YUPIK), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/yupikcameraconf.h
endif

ifeq ($(CONFIG_ARCH_SM6150), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/config/sm6150cameraconf.h
endif

endif

ifneq (,$(filter $(CONFIG_SPECTRA_CAMERA), y m))
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/include/uapi

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/include/uapi \
                -I$(srctree)/techpack/camera-legacy/$(BOARD_CONFIG_CAMERA_KERNEL_NAME)/include
obj-y += drivers/
else
$(info Target not found)
endif
