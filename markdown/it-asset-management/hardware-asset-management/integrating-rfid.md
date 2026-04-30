---
title: Integrating Zebra technology RFID system
description: Integrating a Zebra technology Radio Frequency Identification \(RFID\) system with your ServiceNow instance enables you to identify , track, and manage your hardware asset locations automatically.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Integrating Zebra technology RFID system

Integrating a Zebra technology Radio Frequency Identification \(RFID\) system with your ServiceNow instance enables you to identify , track, and manage your hardware asset locations automatically.

After the asset integration with Zebra technology RFID system is successful, you can view the RFID Tag information such as zone group, zone, and locations mapped with your assets. The RFID information is mapped to the Asset \[alm\_asset\] table according to the serial number of the asset. For more information about the Asset management tables, see [Installed with Asset Management](../../asset-management/reference/r_InstalledWithAssetManagement.md).

**Note:** If the asset is excluded, the RFID information isn't mapped to the Asset \[alm\_asset\] table according to the serial number of the asset. For more information about asset exclusion, see [Hardware Asset Management license exclusion](ham-license-exclusion.md).

The data from the Zebra technology RFID system is imported to ServiceNow regularly. Any data change in the RFID system is updated in your ServiceNow instance.

The RFID asset \[rfid\_asset\] table stores the RFID information of assets. For more information about viewing the RFID information, see [View RFID information of assets](../task/view-rfid-info.md).

