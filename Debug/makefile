################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
Servo_for_jobTest.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Servo_for_jobTest.list \


# All Target
all: Servo_for_jobTest.elf secondary-outputs

# Tool invocations
Servo_for_jobTest.elf: $(OBJS) $(USER_OBJS) C:\Users\Ivan\STM32CubeIDE\workspace_1.1.0\Servo_for_jobTest\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Servo_for_jobTest.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Ivan\STM32CubeIDE\workspace_1.1.0\Servo_for_jobTest\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Servo_for_jobTest.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Servo_for_jobTest.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Servo_for_jobTest.list"
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
