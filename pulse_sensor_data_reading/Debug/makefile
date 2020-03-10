################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F3xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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
pulse_sensor_data_reading.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
pulse_sensor_data_reading.list \


# All Target
all: pulse_sensor_data_reading.elf secondary-outputs

# Tool invocations
pulse_sensor_data_reading.elf: $(OBJS) $(USER_OBJS) Z:\projects\NucleoSTM32\pulse_sensor_data_reading\STM32F303RETX_FLASH.ld
	arm-none-eabi-gcc -o "pulse_sensor_data_reading.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"Z:\projects\NucleoSTM32\pulse_sensor_data_reading\STM32F303RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="pulse_sensor_data_reading.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

pulse_sensor_data_reading.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "pulse_sensor_data_reading.list"
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
