################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/MCP2515/subdir.mk
-include Core/Src/LCD_ILI9341/LCDTools/subdir.mk
-include Core/Src/LCD_ILI9341/LCDCore/subdir.mk
-include Core/Src/FlashMemory/subdir.mk
-include Core/Src/Encoder/subdir.mk
-include Core/Src/CControl/Sources/SystemIdentification/subdir.mk
-include Core/Src/CControl/Sources/Optimization/subdir.mk
-include Core/Src/CControl/Sources/Miscellaneous/subdir.mk
-include Core/Src/CControl/Sources/LinearAlgebra/subdir.mk
-include Core/Src/CControl/Sources/ControlEngineering/subdir.mk
-include Core/Src/CControl/Sources/ArtificialIntelligence/subdir.mk
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
Model\ Reference\ Adaptive\ CAN-Bus\ Controller.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Model\ Reference\ Adaptive\ CAN-Bus\ Controller.list \

OBJCOPY_BIN += \
Model\ Reference\ Adaptive\ CAN-Bus\ Controller.bin \


# All Target
all: Model\ Reference\ Adaptive\ CAN-Bus\ Controller.elf secondary-outputs

# Tool invocations
Model\ Reference\ Adaptive\ CAN-Bus\ Controller.elf: $(OBJS) $(USER_OBJS) /home/dell/Dokument/STM32-Workspace/Model\ Reference\ Adaptive\ CAN-Bus\ Controller/STM32F401RETX_FLASH.ld
	arm-none-eabi-gcc -o "Model Reference Adaptive CAN-Bus Controller.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/dell/Dokument/STM32-Workspace/Model Reference Adaptive CAN-Bus Controller/STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Model Reference Adaptive CAN-Bus Controller.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Model\ Reference\ Adaptive\ CAN-Bus\ Controller.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Model Reference Adaptive CAN-Bus Controller.list"
	@echo 'Finished building: $@'
	@echo ' '

Model\ Reference\ Adaptive\ CAN-Bus\ Controller.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Model Reference Adaptive CAN-Bus Controller.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
