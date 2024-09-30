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
   
This **cmsis_core** MCU component repository is one element **common to all** STM32Cube MCU embedded software packages, providing the **cmsis core** part. 

> [!NOTE]
> This repository is a **subset** of the [CMSIS_5/CMSIS](https://github.com/ARM-software/CMSIS_5/tree/develop/CMSIS) directory. Some subdirectories like `./CMSIS/DAP` or `./CMSIS/DoxyGen` have been discarded as not used in the STM32Cube firmware. The `./CMSIS/Driver` subdirectory has also been discarded as it should be replaced by a `../STM32XXxx_HAL_Driver` directory in the complete file tree of a firmware.

> [!NOTE]
> Starting from version `5.1.0`, a `Core_A/Include` directory has been introduced to support Cortex-A cores. However, this has no impact on Cortex-M-based user applications.

> [!IMPORTANT]
> Starting from version `5.8.0`, Arm **removed** the precompiled **DSP** libraries from the `./DSP/Lib` subdirectory.

> [!IMPORTANT]
> During the successive deliveries from ARM Limited, an update has been introduced with version `5.0`. **A break** of directory tree compatibility has been introduced: the files under the `./Include` directory have been moved to anoter directory, `./Core/Include`.
>
> In order to **preserve compatibility**, the **cmsis_core** repository provided by *STMicroelectronics* introduces an `./Include` directory at its root, where there is a copy of the content of the `./Core/Include` directory provided by ARM.

> [!TIP]
> With each official tag (**e.g.**, `v4.5`), specific flavors of the CMSIS Core are proposed, one for each supported Cortex-M core. Each specific flavor is identified by a tag suffixed *_cmX* (**e.g.**, tag `v4.5_cm3` refers to version `4.5.0` of the CMSIS Core specific to Cortex-M3).
>
> These specific flavors are **size-optimized** as their `./DSP/Lib` subdirectory, the **most voluminous**, only contains the precompiled libraries for the intended Cortex-M core, those for other Cortex-M cores being removed.
>
> All tags suffixed the same are part of a dedicated branch (**e.g.**, `v4.5_cm3`, `v5.4.0_cm3`, `v5.6.0_cm3` are part of the `cm3` branch).

### Caution 

It is mandatory to select one Tag version of the **cmsis_core**, never select the default master branch in your projects.

## Compatibility information

It is **crucial** that you use a consistent set of versions for the CMSIS Core - CMSIS Device, as mentioned in the release note of the [firmware](https://github.com/STMicroelectronics/STM32Cube_MCU_Overall_Offer/blob/master/README.md#stm32cube-mcu-packages) you are using.

## Troubleshooting

Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) guide.
