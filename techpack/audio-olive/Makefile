# auto-detect subdirs
ifeq ($(CONFIG_ARCH_SDM845), y)
include $(srctree)/techpack/audio-olive/config/sdm845auto.conf
export
endif
ifeq ($(CONFIG_ARCH_SDM439), y)
include $(srctree)/techpack/audio-olive/config/sdm450auto.conf
export
endif
ifeq ($(CONFIG_ARCH_SDM670), y)
include $(srctree)/techpack/audio-olive/config/sdm710auto_static.conf
export
endif
ifeq ($(CONFIG_ARCH_SDXPOORWILLS), y)
include $(srctree)/techpack/audio-olive/config/sdxpoorwillsauto.conf
export
endif

# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/audio-olive/include/uapi \

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/audio-olive/include/uapi \
                -I$(srctree)/techpack/audio-olive/include

ifeq ($(CONFIG_ARCH_SDM845), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio-olive/config/sdm845autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDM439), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio-olive/config/sdm450autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDM670), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio-olive/config/sdm710autoconf.h
endif
ifeq ($(CONFIG_ARCH_SDXPOORWILLS), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio-olive/config/sdxpoorwillsautoconf.h
endif

obj-y += asoc/
obj-y += dsp/
obj-y += ipc/
obj-y += soc/
