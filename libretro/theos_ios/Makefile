DEPLOYMENT_IOSVERSION = 5.0
TARGET = iphone:latest:$(DEPLOYMENT_IOSVERSION)
ARCHS = armv7 armv7s
TARGET_IPHONEOS_DEPLOYMENT_VERSION=$(DEPLOYMENT_IOSVERSION)
THEOS_BUILD_DIR := objs
include $(THEOS)/makefiles/common.mk

LIBRARY_NAME = snes9x_next_libretro_ios
CORE_DIR := ../..
HAVE_GRIFFIN = 1

include ../../Makefile.common

${LIBRARY_NAME}_FILES = $(SOURCES_CXX) $(SOURCES_C)

COMMON_FLAGS = -DIOS -DARM -D__LIBRETRO__ -DHAVE_STRINGS_H -DHAVE_STDINT_H -DRIGHTSHIFT_IS_SAR -DINLINE=inline -DFRONTEND_SUPPORTS_RGB565 $(INCFLAGS) -I$(THEOS_INCLUDE_PATH) -Wno-error

$(LIBRARY_NAME)_CFLAGS += $(COMMON_FLAGS)

include $(THEOS_MAKE_PATH)/library.mk
