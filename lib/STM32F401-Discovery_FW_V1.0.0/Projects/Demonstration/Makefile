# put your *.c source files here, make should handle the rest!
SRCS=main.c

# all the files will be generated with this name (main.elf, main.bin, main.hex, etc)
PROJ_NAME=main

# Target MCU. STM32F40_41xxx / STM32F427_437xx / STM32F429_439xx / STM32F401xx
# See */CMSIS/Device/ST/*/stm32f*.h
MCU=STM32F401xx

###################################################

# Build artifact location
BUILD_DIR=build

# External libraries
LIBRARIES = ../../..

# Libraries from ST / ARM
ST_FIRMWARE = $(LIBRARIES)/STM32F401-Discovery_FW_V1.0.0

CMSIS = $(ST_FIRMWARE)/Libraries/CMSIS
STD_PERIPH_DRIVER = $(ST_FIRMWARE)/STM32F4xx_StdPeriph_Driver

###################################################

# Location of linker scripts. Linker script is $(MCU).ld
LINKER_SCRIPT_DIR = $(LIBRARIES)/linker

STARTUP_SCRIPT = $(CMSIS)/Device/ST/STM32F4xx/Source/Templates/gcc_ride7/startup_stm32f401xx.s

###################################################

CC=arm-none-eabi-gcc
GDB=arm-none-eabi-gdb
OBJCOPY=arm-none-eabi-objcopy
OBJDUMP=arm-none-eabi-objdump
SIZE=arm-none-eabi-size

# SRCS   += $(ST_FIRMWARE)/system_stm32f4xx.c

CFLAGS  = -Wall -g -std=c99 -Os  
CFLAGS += -mlittle-endian -mcpu=cortex-m4  -march=armv7e-m -mthumb
CFLAGS += -mfpu=fpv4-sp-d16 -mfloat-abi=hard
CFLAGS += -ffunction-sections -fdata-sections

LDFLAGS += -Wl,--gc-sections -Wl,-Map=$(BUILD_DIR)/$(PROJ_NAME).map

CFLAGS += -DUSE_STDPERIPH_DRIVER
CFLAGS += -DSTM32F401xx
CFLAGS += -DUSE_USB_OTG_FS
CFLAGS += -DUSE_STM32F401
CFLAGS += -DI2S_INTERRUPT

###################################################

vpath %.a $(STD_PERIPH_LIB)

ROOT=$(shell pwd)

CFLAGS += -D $(MCU)
CFLAGS += -L $(ST_FIRMWARE)
CFLAGS += -I inc 
CFLAGS += -I .
CFLAGS += -I $(CMSIS)/Include
CFLAGS += -I $(CMSIS)/Device/ST/STM32F4xx/Include
CFLAGS += -I $(ST_FIRMWARE)
CFLAGS += -I $(ST_FIRMWARE)/Libraries/stm32f4xx_StdPeriph_Driver/inc
CFLAGS += -I $(ST_FIRMWARE)/Utilities/STM32F401-Discovery
CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_OTG_Driver/inc
CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Core/inc
# CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/audio/inc
# CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/cdc/inc
# CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/dfu/inc
CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/hid/inc
# CFLAGS += -I $(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/msc/inc
# CFLAGS += -I $(CMSIS)/Include
# CFLAGS += -I $(STD_PERIPH_LIB)/Libraries/STM32F4xx_StdPeriph_Driver/inc
# CFLAGS += -I $(STD_PERIPH_LIB)/Projects/Demonstration/stm32f4xx_conf.h

SRCS += stm32f401_discovery.c  \
stm32f401_discovery_audio_codec.c \
stm32f401_discovery_l3gd20.c \
stm32f401_discovery_lsm303dlhc.c \
stm32f4xx_it.c \
system_stm32f4xx.c \
usb_bsp.c \
usbd_desc.c \
usbd_usr.c \
selftest.c

# SRCS += stm32f0_discovery.c stm32f0xx_it.c

SRCS += \
$(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Class/hid/src/usbd_hid_core.c

SRCS += \
$(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Core/src/usbd_core.c \
$(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Core/src/usbd_ioreq.c \
$(ST_FIRMWARE)/Libraries/STM32_USB_Device_Library/Core/src/usbd_req.c

SRCS += \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_core.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_keybd.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_mouse.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_bot.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_core.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_fatfs.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_scsi.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Core/src/usbh_core.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Core/src/usbh_hcs.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Core/src/usbh_ioreq.c \
#$(ST_FIRMWARE)/Libraries/STM32_USB_HOST_Library/Core/src/usbh_stdreq.c

SRCS += \
$(ST_FIRMWARE)/Libraries/STM32_USB_OTG_Driver/src/usb_core.c \
$(ST_FIRMWARE)/Libraries/STM32_USB_OTG_Driver/src/usb_dcd.c \
$(ST_FIRMWARE)/Libraries/STM32_USB_OTG_Driver/src/usb_dcd_int.c

OBJS = $(SRCS:.c=.o)
DEPS = $(SRCS:.c=.d)

###################################################

.PHONY: all proj program debug clean reallyclean

all: firmware proj

-include $(DEPS)

firmware: $(ST_FIRMWARE)
	$(MAKE) -C $(ST_FIRMWARE) MCU=$(MCU)

proj: $(BUILD_DIR) $(BUILD_DIR)/$(PROJ_NAME).elf

$(BUILD_DIR):
	mkdir -p $(BUILD_DIR)
	mkdir -p $(BUILD_DIR)/deps $(BUILD_DIR)/objs

$(BUILD_DIR)/objs/%.o : %.c $(BUILD_DIR)
	$(CC) $(CFLAGS) -c -o $@ $< -MMD -MF $(BUILD_DIR)/deps/$(*F).d

$(BUILD_DIR)/$(PROJ_NAME).elf: $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) $^ -o $@ $(STARTUP_SCRIPT) -lstm32f4 -T$(LINKER_SCRIPT_DIR)/$(MCU).ld
	$(OBJCOPY) -O ihex $(BUILD_DIR)/$(PROJ_NAME).elf $(BUILD_DIR)/$(PROJ_NAME).hex
	$(OBJCOPY) -O binary $(BUILD_DIR)/$(PROJ_NAME).elf $(BUILD_DIR)/$(PROJ_NAME).bin
	$(OBJDUMP) -St $(BUILD_DIR)/$(PROJ_NAME).elf >$(BUILD_DIR)/$(PROJ_NAME).lst
	$(SIZE) $(BUILD_DIR)/$(PROJ_NAME).elf

program: all
	@sleep 1
	st-flash write `pwd`/$(BUILD_DIR)/$(PROJ_NAME).bin 0x08000000

debug: program
	$(GDB) -x extra/gdb_cmds $(PROJ_NAME).elf

clean:
	find ./ -name '*~' | xargs rm -f	
	rm -rf $(BUILD_DIR)

reallyclean: clean
	$(MAKE) -C $(ST_FIRMWARE) clean
