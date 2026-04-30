---
title: Create a firmware model for the firmware embedded into your Operational Technology \(OT\) assets
description: Create a firmware model for the firmware that's embedded into your OT assets if the model isn't already represented in the Enterprise Asset Management Content Service.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for your operational technology \(OT\) assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a firmware model for the firmware embedded into your Operational Technology \(OT\) assets

Create a firmware model for the firmware that's embedded into your OT assets if the model isn't already represented in the Enterprise Asset Management Content Service.

## Before you begin

**Important:** The OT Asset Management application must be activated to access the OT Asset Workspace. For details, see [Install OT Asset Management](install-otam.md).

The firmware product and the firmware version details should be available in the Enterprise Asset Management Content Service. If not, you can also create the firmware product and the firmware version for your firmware model. For more details, see [Create a custom firmware product for your operational technology \(OT\) assets](create-custom-firmware-product-ot-assets.md) and [Create a custom firmware version for your operational technology \(OT\) assets](create-custom-firmware-version-ot-assets.md).

Role required: sn\_otam.ot\_asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **OT Model Management**.

2.  Select the **Firmware** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display name|Name of the firmware model. This field is populated automatically with a value that's based on the **Publisher**, **Product**, and **Version** fields.|
    |Publisher|Manufacturer of the firmware model.|
    |Product|Name of the firmware product. This field is required.|
    |Version|Version of the firmware.This field is required.|
    |Next version available|Option that indicates if the next firmware version is available.|
    |Manually created|Option that indicates that the firmware version is created manually. The check box is automatically selected.|

5.  Select **Save**.


## Result

-   A firmware model is created and listed in the **Firmware** tab.
-   The firmware model record displays the following related lists:
    -   Discovered firmware
    -   Firmware installations
    -   Firmware model lifecycles
    -   Knowledge
-   The lifecycle phases associated with the firmware model are listed in **Firmware model lifecycles** tab only if that firmware version has lifecycles defined in the Firmware lifecycle definition \[sn\_itam\_firmware\_lifecycle\_def\] table.

