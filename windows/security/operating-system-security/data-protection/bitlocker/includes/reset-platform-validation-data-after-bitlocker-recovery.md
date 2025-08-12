---
author: paolomatarazzo
ms.author: paoloma
ms.date: 10/30/2023
ms.topic: include
---

### Reset platform validation data after BitLocker recovery

This policy setting determines if platform validation data should refresh when Windows is started following a BitLocker recovery. A platform validation data profile consists of the values in a set of Platform Configuration Register (PCR) indices that range from 0 to 23.

If you enable this policy setting, platform validation data is refreshed when Windows is started following BitLocker recovery. This is the default behavior.\
If you disable this policy setting, platform validation data won't be refreshed when Windows is started following BitLocker recovery.

For more information about the recovery process, see the [BitLocker recovery overview](../recovery-overview.md).

|  | Path |
|--|--|
| **CSP** | Not available |
| **GPO** | **Computer Configuration** > **Administrative Templates** > **Windows Components** > **BitLocker Drive Encryption** > **Operating System Drives** |
