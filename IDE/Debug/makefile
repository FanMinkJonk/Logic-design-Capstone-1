################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Logic-design-capstone
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Logic-design-capstone.elf \

MAP_FILES += \
Logic-design-capstone.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Logic-design-capstone.list \

OBJCOPY_HEX += \
Logic-design-capstone.hex \

OBJCOPY_BIN += \
Logic-design-capstone.bin \


# All Target
all: main-build

# Main-build Target
main-build: Logic-design-capstone.elf secondary-outputs

# Tool invocations
Logic-design-capstone.elf Logic-design-capstone.map: $(OBJS) $(USER_OBJS) E:\Documents\5th\ semester\ projects\Capstone\ 1.\ Logic\ design\Git\ main\IDE\STM32F103RBTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Logic-design-capstone.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\Documents\5th semester projects\Capstone 1. Logic design\Git main\IDE\STM32F103RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Logic-design-capstone.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Logic-design-capstone.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Logic-design-capstone.list"
	@echo 'Finished building: $@'
	@echo ' '

Logic-design-capstone.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Logic-design-capstone.hex"
	@echo 'Finished building: $@'
	@echo ' '

Logic-design-capstone.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Logic-design-capstone.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Logic-design-capstone.bin Logic-design-capstone.elf Logic-design-capstone.hex Logic-design-capstone.list Logic-design-capstone.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
