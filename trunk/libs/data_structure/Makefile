LOCAL_DIR := $(PWD)

ifndef FINS_ROOT_DIR
export FINS_ROOT_DIR := $(abspath $(LOCAL_DIR)/../../..)
endif

# fins.mk contains the compiler and linker options for each target platform
include $(FINS_ROOT_DIR)/settings.finsmk

#Name of the module
LOCAL_NAME := data_structure
ifdef BUILD_FOR_ANDROID_ARM
LOCAL_LIBS := config common
else
LOCAL_LIBS := common
endif
LOCAL_OBJS := queue.o finsqueue.o finsmodule.o
LOCAL_INCS := .
LOCAL_CFLAGS := -fpic
LOCAL_LDFLAGS := -lc -ldl

include $(LIBS_DIR)/make_library.finsmk