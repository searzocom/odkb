################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/HID/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
odkbfw.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
odkbfw.list \


# All Target
all: odkbfw.elf secondary-outputs

# Tool invocations
odkbfw.elf: $(OBJS) $(USER_OBJS) G:\seaf\cloud\odkb_top\fw\src\ide\STM32F103RCTX_FLASH.ld
	arm-none-eabi-gcc -o "odkbfw.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"G:\seaf\cloud\odkb_top\fw\src\ide\STM32F103RCTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="odkbfw.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

odkbfw.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "odkbfw.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
