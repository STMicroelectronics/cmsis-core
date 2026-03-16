# origin-pack: STMicroelectronics::CMSIS@6.3.0
# file-format: 1.0.0
project(STMicroelectronics_CMSIS_6_3_0)
cmake_minimum_required(VERSION 3.20)
add_library(STMicroelectronics_CMSIS_6_3_0 INTERFACE)

# List of all CMSIS properties that influence conditions for this package
if(NOT DEFINED CMSIS_Dcore)
  set(CMSIS_Dcore "CMSIS_Dcore not set")
  message(DEBUG "CMSIS_Dcore is not set to any value")
endif()

if(NOT DEFINED CMSIS_Dsecure)
  set(CMSIS_Dsecure "CMSIS_Dsecure not set")
  message(DEBUG "CMSIS_Dsecure is not set to any value")
endif()

if(NOT DEFINED CMSIS_Dtz)
  set(CMSIS_Dtz "CMSIS_Dtz not set")
  message(DEBUG "CMSIS_Dtz is not set to any value")
endif()


# Device specific defined symbols








# Enable all components in this package
if(CMSIS_ENTIRE_STMicroelectronics_CMSIS_6_3_0)
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:CORE#Cversion:6.2.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:CORE#Cversion:6.2.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:Device#Cgroup:IRQ Controller#Csub:GIC#Cversion:1.2.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:SysTick#Cversion:1.0.5")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:Private Timer#Cversion:1.0.2")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:Generic Physical Timer#Cversion:1.0.1")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USART#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:SPI#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:SAI#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:I2C#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:CAN#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Flash#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:MCI#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:NAND#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet MAC#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet PHY#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USB Device#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USB Host#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:GPIO#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:WiFi#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:VIO#Csub:Custom#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:VIO#Csub:Virtual#Cversion:1.0.0")
  list(APPEND CMSIS_COMPONENTS_LIST "Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:vStream#Csub:Custom#Cversion:1.0.0")
endif()

# All conditions used by this package

# condition: STMicroelectronics.CMSIS.6.3.0:ARMv6-M Device
# description: Armv6-M architecture based device
if((CMSIS_Dcore STREQUAL "Cortex-M0" OR CMSIS_Dcore STREQUAL "Cortex-M1" OR CMSIS_Dcore STREQUAL "Cortex-M0+" OR CMSIS_Dcore STREQUAL "SC000"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv6-M_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv6-M_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv6-M_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv6_7_8-M Device
# description: Armv6_7_8-M architecture based device
if(((CMSIS_Dcore STREQUAL "Cortex-M0" OR CMSIS_Dcore STREQUAL "Cortex-M1" OR CMSIS_Dcore STREQUAL "Cortex-M0+" OR CMSIS_Dcore STREQUAL "SC000") OR (CMSIS_Dcore STREQUAL "Cortex-M3" OR CMSIS_Dcore STREQUAL "Cortex-M4" OR CMSIS_Dcore STREQUAL "Cortex-M7" OR CMSIS_Dcore STREQUAL "SC300") OR ((CMSIS_Dcore STREQUAL "ARMV8MBL" OR CMSIS_Dcore STREQUAL "Cortex-M23") OR (CMSIS_Dcore STREQUAL "ARMV8MML" OR CMSIS_Dcore STREQUAL "Cortex-M33" OR CMSIS_Dcore STREQUAL "Cortex-M35P" OR CMSIS_Dcore STREQUAL "Star-MC1") OR (CMSIS_Dcore STREQUAL "ARMV81MML" OR CMSIS_Dcore STREQUAL "Cortex-M52" OR CMSIS_Dcore STREQUAL "Cortex-M55" OR CMSIS_Dcore STREQUAL "Cortex-M85" OR CMSIS_Dcore STREQUAL "Star-MC3"))))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv7-A Device
# description: Armv7-A architecture based device
if((CMSIS_Dcore STREQUAL "Cortex-A5" OR CMSIS_Dcore STREQUAL "Cortex-A7" OR CMSIS_Dcore STREQUAL "Cortex-A9"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv7-M Device
# description: Armv7-M architecture based device
if((CMSIS_Dcore STREQUAL "Cortex-M3" OR CMSIS_Dcore STREQUAL "Cortex-M4" OR CMSIS_Dcore STREQUAL "Cortex-M7" OR CMSIS_Dcore STREQUAL "SC300"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv7-M_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv7-M_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv7-M_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv8-M Device
# description: Armv8-M architecture based device
if(((CMSIS_Dcore STREQUAL "ARMV8MBL" OR CMSIS_Dcore STREQUAL "Cortex-M23") OR (CMSIS_Dcore STREQUAL "ARMV8MML" OR CMSIS_Dcore STREQUAL "Cortex-M33" OR CMSIS_Dcore STREQUAL "Cortex-M35P" OR CMSIS_Dcore STREQUAL "Star-MC1") OR (CMSIS_Dcore STREQUAL "ARMV81MML" OR CMSIS_Dcore STREQUAL "Cortex-M52" OR CMSIS_Dcore STREQUAL "Cortex-M55" OR CMSIS_Dcore STREQUAL "Cortex-M85" OR CMSIS_Dcore STREQUAL "Star-MC3")))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-M_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv8-M_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-M_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv8-MBL Device
# description: Armv8-M base line architecture based device
if((CMSIS_Dcore STREQUAL "ARMV8MBL" OR CMSIS_Dcore STREQUAL "Cortex-M23"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-MBL_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv8-MBL_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-MBL_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv8-MML Device
# description: Armv8-M main line architecture based device
if((CMSIS_Dcore STREQUAL "ARMV8MML" OR CMSIS_Dcore STREQUAL "Cortex-M33" OR CMSIS_Dcore STREQUAL "Cortex-M35P" OR CMSIS_Dcore STREQUAL "Star-MC1"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-MML_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv8-MML_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv8-MML_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:ARMv81-MML Device
# description: Armv8.1-M main line architecture based device
if((CMSIS_Dcore STREQUAL "ARMV81MML" OR CMSIS_Dcore STREQUAL "Cortex-M52" OR CMSIS_Dcore STREQUAL "Cortex-M55" OR CMSIS_Dcore STREQUAL "Cortex-M85" OR CMSIS_Dcore STREQUAL "Star-MC3"))
  set(STMicroelectronics.CMSIS.6.3.0_ARMv81-MML_Device "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_ARMv81-MML_Device enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_ARMv81-MML_Device 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:OS Tick GTIM
# description: Components required for OS Tick Generic Physical Timer
if(CMSIS_Dcore STREQUAL "Cortex-A7")
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_GTIM "$<NOT:$<STREQUAL:$<FILTER:${CMSIS_COMPONENTS_LIST},INCLUDE,.*Cclass:Device#.*Cgroup:IRQ Controller(#.*|$)>,>>")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_OS_Tick_GTIM enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_GTIM 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:OS Tick PTIM
# description: Components required for OS Tick Private Timer
if((CMSIS_Dcore STREQUAL "Cortex-A5" OR CMSIS_Dcore STREQUAL "Cortex-A9"))
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_PTIM "$<NOT:$<STREQUAL:$<FILTER:${CMSIS_COMPONENTS_LIST},INCLUDE,.*Cclass:Device#.*Cgroup:IRQ Controller(#.*|$)>,>>")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_OS_Tick_PTIM enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_PTIM 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:OS Tick SysTick
# description: Components required for OS Tick SysTick Timer
if(((CMSIS_Dcore STREQUAL "Cortex-M0" OR CMSIS_Dcore STREQUAL "Cortex-M1" OR CMSIS_Dcore STREQUAL "Cortex-M0+" OR CMSIS_Dcore STREQUAL "SC000") OR (CMSIS_Dcore STREQUAL "Cortex-M3" OR CMSIS_Dcore STREQUAL "Cortex-M4" OR CMSIS_Dcore STREQUAL "Cortex-M7" OR CMSIS_Dcore STREQUAL "SC300") OR ((CMSIS_Dcore STREQUAL "ARMV8MBL" OR CMSIS_Dcore STREQUAL "Cortex-M23") OR (CMSIS_Dcore STREQUAL "ARMV8MML" OR CMSIS_Dcore STREQUAL "Cortex-M33" OR CMSIS_Dcore STREQUAL "Cortex-M35P" OR CMSIS_Dcore STREQUAL "Star-MC1") OR (CMSIS_Dcore STREQUAL "ARMV81MML" OR CMSIS_Dcore STREQUAL "Cortex-M52" OR CMSIS_Dcore STREQUAL "Cortex-M55" OR CMSIS_Dcore STREQUAL "Cortex-M85" OR CMSIS_Dcore STREQUAL "Star-MC3"))))
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_SysTick "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_OS_Tick_SysTick enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_OS_Tick_SysTick 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:TZ Secure
# description: TrustZone (Secure)
if(((CMSIS_Dsecure STREQUAL "Secure" OR CMSIS_Dsecure STREQUAL "Secure-only") AND 
   CMSIS_Dtz STREQUAL "TZ"))
  set(STMicroelectronics.CMSIS.6.3.0_TZ_Secure "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_TZ_Secure enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_TZ_Secure 0)
endif()


# condition: STMicroelectronics.CMSIS.6.3.0:TrustZone
# description: TrustZone
if((CMSIS_Dtz STREQUAL "TZ" AND NOT 
   CMSIS_Dsecure STREQUAL "TZ-disabled"))
  set(STMicroelectronics.CMSIS.6.3.0_TrustZone "1")
  message(DEBUG "CMSIS condition STMicroelectronics.CMSIS.6.3.0_TrustZone enabled")
else()
  set(STMicroelectronics.CMSIS.6.3.0_TrustZone 0)
endif()

# Files and components in this package
if("Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:CORE#Cversion:6.2.0" IN_LIST CMSIS_COMPONENTS_LIST)  # CMSIS-CORE for Cortex-M, SC000, SC300, Star-MC, ARMv8-M, ARMv8.1-M
  message(DEBUG "Using component CMSIS_CORE_6_2_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device}:-DCMSIS_USE_CMSIS_CORE_6_2_0=1>")
  target_include_directories(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/Core/Include/>")
  target_include_directories(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<$<AND:${STMicroelectronics.CMSIS.6.3.0_ARMv6_7_8-M_Device},${STMicroelectronics.CMSIS.6.3.0_TrustZone}>:${CMAKE_CURRENT_LIST_DIR}/CMSIS/Core/Include>")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:CORE#Cversion:6.2.0" IN_LIST CMSIS_COMPONENTS_LIST)  # CMSIS-CORE for Cortex-A
  message(DEBUG "Using component CMSIS_CORE_6_2_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device}:-DCMSIS_USE_CMSIS_CORE_6_2_0=1>")
  target_include_directories(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/Core/Include/>")
endif()

if("Cvendor:STMicroelectronics#Cclass:Device#Cgroup:IRQ Controller#Csub:GIC#Cversion:1.2.0" IN_LIST CMSIS_COMPONENTS_LIST)  # IRQ Controller implementation using GIC
  message(DEBUG "Using component Device_IRQ_Controller_GIC_1_2_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device}:-DCMSIS_USE_Device_IRQ_Controller_GIC_1_2_0=1>")
  target_sources(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_ARMv7-A_Device}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/Core/Source/irq_ctrl_gic.c>")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:SysTick#Cversion:1.0.5" IN_LIST CMSIS_COMPONENTS_LIST)  # OS Tick implementation using Cortex-M SysTick Timer
  message(DEBUG "Using component CMSIS_OS_Tick_SysTick_1_0_5")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_SysTick}:-DCMSIS_USE_CMSIS_OS_Tick_SysTick_1_0_5=1>")
  target_sources(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_SysTick}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/RTOS2/Source/os_systick.c>")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:Private Timer#Cversion:1.0.2" IN_LIST CMSIS_COMPONENTS_LIST)  # OS Tick implementation using Private Timer
  message(DEBUG "Using component CMSIS_OS_Tick_Private_Timer_1_0_2")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_PTIM}:-DCMSIS_USE_CMSIS_OS_Tick_Private_Timer_1_0_2=1>")
  target_sources(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_PTIM}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/RTOS2/Source/os_tick_ptim.c>")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS#Cgroup:OS Tick#Csub:Generic Physical Timer#Cversion:1.0.1" IN_LIST CMSIS_COMPONENTS_LIST)  # OS Tick implementation using Generic Physical Timer
  message(DEBUG "Using component CMSIS_OS_Tick_Generic_Physical_Timer_1_0_1")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_GTIM}:-DCMSIS_USE_CMSIS_OS_Tick_Generic_Physical_Timer_1_0_1=1>")
  target_sources(STMicroelectronics_CMSIS_6_3_0 INTERFACE "$<${STMicroelectronics.CMSIS.6.3.0_OS_Tick_GTIM}:${CMAKE_CURRENT_LIST_DIR}/CMSIS/RTOS2/Source/os_tick_gtim.c>")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USART#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_USART.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_USART_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_USART_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:SPI#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_SPI.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_SPI_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_SPI_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:SAI#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_SAI.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_SAI_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_SAI_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:I2C#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_I2C.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_I2C_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_I2C_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:CAN#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_CAN.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_CAN_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_CAN_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Flash#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_Flash.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_Flash_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_Flash_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:MCI#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_MCI.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_MCI_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_MCI_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:NAND#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_NAND.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_NAND_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_NAND_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_ETH_PHY/MAC.h files and code templates for custom implementation
  message(DEBUG "Using component CMSIS_Driver_Ethernet_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_Ethernet_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet MAC#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_ETH_MAC.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_Ethernet_MAC_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_Ethernet_MAC_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:Ethernet PHY#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_ETH_PHY.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_Ethernet_PHY_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_Ethernet_PHY_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USB Device#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_USBD.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_USB_Device_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_USB_Device_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:USB Host#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_USBH.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_USB_Host_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_USB_Host_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:GPIO#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_GPIO.h file and code template for custom implementation
  message(DEBUG "Using component CMSIS_Driver_GPIO_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_GPIO_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:WiFi#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Access to #include Driver_WiFi.h file
  message(DEBUG "Using component CMSIS_Driver_WiFi_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_WiFi_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:VIO#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Virtual I/O custom implementation template
  message(DEBUG "Using component CMSIS_Driver_VIO_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_VIO_Custom_1_0_0=1")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:VIO#Csub:Virtual#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Virtual I/O implementation using memory only
  message(DEBUG "Using component CMSIS_Driver_VIO_Virtual_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_VIO_Virtual_1_0_0=1")
  target_sources(STMicroelectronics_CMSIS_6_3_0 INTERFACE "${CMAKE_CURRENT_LIST_DIR}/CMSIS/Driver/VIO/Source/vio_memory.c")
endif()

if("Cvendor:STMicroelectronics#Cclass:CMSIS Driver#Cgroup:vStream#Csub:Custom#Cversion:1.0.0" IN_LIST CMSIS_COMPONENTS_LIST)  # Virtual Streaming interface Driver custom implementation template
  message(DEBUG "Using component CMSIS_Driver_vStream_Custom_1_0_0")
  target_compile_definitions(STMicroelectronics_CMSIS_6_3_0 INTERFACE "-DCMSIS_USE_CMSIS_Driver_vStream_Custom_1_0_0=1")
endif()

