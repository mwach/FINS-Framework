LOCAL_DIR := $(PWD)

ifndef FINS_ROOT_DIR
export FINS_ROOT_DIR := $(abspath $(LOCAL_DIR)/../../..)
endif

# fins.mk contains the compiler and linker options for each target platform
include $(FINS_ROOT_DIR)/settings.finsmk

#Name of the module, must be equal to folder
LOCAL_NAME := rtm
LOCAL_OBJS := rtm.o rtm_process.o
LOCAL_INCS := .
LOCAL_CFLAGS := -fpic

ifdef BUILD_FOR_ANDROID_ARM
LOCAL_LIBS := config common data_structure
LOCAL_LDFLAGS := -lc
else
LOCAL_LIBS := data_structure 
LOCAL_LDFLAGS := -lc -lpthread
endif

include $(MODULES_DIR)/make_module.finsmk