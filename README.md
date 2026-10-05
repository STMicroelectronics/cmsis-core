# STM32Cube CMSIS Core Interface MCU Software Component

![tag](https://img.shields.io/badge/tag-6.3.0-brightgreen.svg)
[![offer](https://img.shields.io/badge/stm32cube_mcu_offer-browse-orange.svg)](https://github.com/STMicroelectronics/STM32Cube_MCU_Overall_Offer)

## Overview

This repository is **cloned** from ARM Limited, strictly compatible. It provides a **subset** of the [CMSIS_5/CMSIS](https://github.com/ARM-software/CMSIS_5/tree/develop/CMSIS) directory, providing a standardized set of header files, startup code, and core access functions that enable initialization, configuration, and control of ARM Cortex processor features.

> [!NOTE]
> Some subdirectories like `./CMSIS/DAP` or `./CMSIS/DoxyGen` have been discarded as not used in the STM32Cube firmware. The `./CMSIS/Driver` subdirectory has also been discarded as it should be replaced by a `../STM32XXxx_HAL_Driver` directory in the complete file tree of a firmware.

> [!NOTE]
> Starting from version `5.1.0`, a `Core_A/Include` directory has been introduced to support Cortex-A cores. However, this has no impact on Cortex-M-based user applications.

> [!IMPORTANT]
> Starting from version `5.8.0`, Arm **removed** the precompiled **DSP** libraries from the `./DSP/Lib` subdirectory and moved them to [this](https://github.com/ARM-software/CMSIS-DSP) dedicated repository.

> [!IMPORTANT]
> During the successive deliveries from ARM Limited, an update has been introduced with version `5.0`. **A break** of directory tree compatibility has been introduced: the files under the `./Include` directory have been moved to anoter directory, `./Core/Include`.
>
> In order to **preserve backward compatibility**, the **cmsis_core** repository provided by *STMicroelectronics* introduces an `./Include` directory at its root, where there is a copy of the content of the `./Core/Include` directory provided by ARM.

> [!TIP]
> With each official tag (**e.g.**, `v4.5`), specific flavors of the CMSIS Core are proposed, one for each supported Cortex-M core. Each specific flavor is identified by a tag suffixed *_cmX* (**e.g.**, tag `v4.5_cm3` refers to version `4.5.0` of the CMSIS Core specific to Cortex-M3).
>
> These specific flavors are **size-optimized** as their `./DSP/Lib` subdirectory, the **most voluminous**, only contains the precompiled libraries for the intended Cortex-M core, those for other Cortex-M cores being removed.
>
> All tags suffixed the same are part of a dedicated branch (**e.g.**, `v4.5_cm3`, `v5.4.0_cm3`, `v5.6.0_cm3` are part of the `cm3` branch).

## Compatibility information

Please refer to the **release note** in the firmware repository for the STM32 series you are using (see the list in the _STM32Cube MCU Offer_). It is **important** to use a **consistent set** of software component versions as specified in the release note.

## Feedback and contributions

Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) guide.
