# CMSIS CORE

![latest tag](https://img.shields.io/github/v/tag/STMicroelectronics/cmsis_core.svg?color=brightgreen)

> [!NOTE]
> The **cmsis_core** repository is delivered to STM32 users. It is cloned from ARM Limited, strictly compatible. 

## Overview

**STM32Cube** is an *STMicroelectronics* original initiative aimed at making life easier for developers by reducing effort, time and cost.

**STM32Cube** covers the overall STM32 products portfolio. It includes a comprehensive embedded software platform delivered for each STM32 series.
   * The CMSIS modules (core and device) corresponding to the ARM(tm) core implemented in this STM32 product.
   * The STM32 HAL-LL drivers, an abstraction layer offering a set of APIs ensuring maximized portability across the STM32 portfolio.
   * The BSP drivers of each evaluation, demonstration, or nucleo board provided for this STM32 series.
   * A consistent set of middleware libraries such as RTOS, USB, FatFS, Graphics, OpenBootloader...
   * A full set of software projects (basic examples, applications, and demonstrations) for each board, each project developed in three flavors using three toolchains (EWARM, MDK-ARM, and STM32CubeIDE).

Two models of publication are proposed for the STM32Cube embedded software:
   * The monolithic **MCU Package**: all STM32Cube software modules of one STM32 series are present (Drivers, Middleware, Projects, Utilities) in the repository (usual name **STM32Cubexx**, xx corresponding to the STM32 series).
   * The **MCU component**: each STM32Cube software module being part of the STM32Cube MCU Package, is delivered as an individual repository, allowing the user to select and get only the required software functions.

## Description
   
This **cmsis_core** MCU component repo is one element of the STM32Cube MCUs embedded software packages, providing the **cmsis core** part. 

> [!IMPORTANT]
> During the successive deliveries from ARM Limited, an update has been introduced with version 5.0. **A break** of directory tree compatibility has been introduced: the files under the `./Include` directory have been moved to directory `./Core/Include`.
> In order to **keep compatibility**, the **cmsis_core** repository provided by *STMicroelectronics* introduces an `./Include` directory at its root, where there is a copy of the content of the `./Core/Include` directory provided by ARM.

> [!NOTE]
> From the version 5.1.0, a Core_A/Include has been introduced to support Cortex_A series. However, this has no impact on Cortex-M-based user applications.

> [!TIP]
> With each official Tag (**e.g.**, `v4.5`), *STMicroelectronics* proposes specific CMSIS Core packages for all supported Cortex-M cores. These specific packages are size-optimized as each one contains only the CMSIS Core files for the targeted Cortex-M. Each specific package is identified by a tag suffixed *_cmX* (**e.g.**, tag `v4.5_cm3` refers to a package containing only version `4.5.0` of CMSIS Core files specific to Cortex-M3 cores, files specific to other Cortex-M cores having been removed).

### Caution 

It is mandatory to select one Tag version of the **cmsis_core**, never select the default master branch in your projects.

## Compatibility information

It is **crucial** that you use a consistent set of versions for the CMSIS Core - CMSIS Device, as mentioned in the release note of the [firmware](https://github.com/STMicroelectronics/STM32Cube_MCU_Overall_Offer/blob/master/README.md#stm32cube-mcu-packages) you are using.

## Troubleshooting

Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) guide.
