---
title: Zebra MotionWorks RFID integration for Enterprise Asset Management
description: You can integrate your ServiceNow instance with third-party Zebra MotionWorks location solutions to import and view real-time radio-frequency identification \(RFID\) location data for your enterprise assets.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Zebra MotionWorks RFID integration for Enterprise Asset Management

You can integrate your ServiceNow instance with third-party Zebra MotionWorks location solutions to import and view real-time radio-frequency identification \(RFID\) location data for your enterprise assets.

RFID is an asset tracking technology that uses radio frequencies to transfer location and identification data for your assets. This data is stored and transferred through RFID tags, which are small devices that are either attached to or embedded in each asset. Each RFID tag consists of the following components:

-   An antenna that receives and transmits radio frequencies so that you can transfer location and identification data for the associated asset. The antenna receives and transmits these radio frequencies each time you scan the RFID tag.
-   A unique microchip or integrated circuit \(IC\) that stores location and identification data for the associated asset.
-   A substrate that holds the other two components together.

Zebra MotionWorks location solutions use RFID technology to track the real-time locations of your assets and inventory automatically. When you integrate your ServiceNow instance with Zebra MotionWorks location solutions, this RFID location data is imported into your instance so that you can identify and track your enterprise assets. Any data changes that Zebra MotionWorks location solutions detect are automatically updated on your ServiceNow instance.

For more information on Zebra MotionWorks, refer to the [Zebra MotionWorks Location Solutions website](https://www.zebra.com/us/en/solutions/intelligent-edge-solutions/rtls.html).

## Importing RFID location data from Zebra MotionWorks location solutions

When you import RFID location data from Zebra MotionWorks location solutions, the data is added to the RFID Stage Asset \[sn\_itam\_common\_rfid\_stg\_asset\] table based on the enterprise assets that it is associated with. The Enterprise Asset Management application automatically creates a separate table entry for each enterprise asset that you import this RFID location data for.

After the RFID location data is added to the RFID Stage Asset \[sn\_itam\_common\_rfid\_stg\_asset\] table, the Enterprise Asset Management application uses the RFID Resource Data transform map to process and then map this data to the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table. However, RFID location data can be mapped to the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table only for enterprise assets that contain serial numbers.

On successful mapping, you can run the **RFID Asset Mapping Job** scheduled job daily or on-demand to then map the resulting data from the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table to the Asset \[alm\_asset\] table. However, this data mapping is dependent on the existence of corresponding asset records within the Asset \[alm\_asset\] table.

-   If a corresponding asset record already exists for an enterprise asset that you want to map data for, it automatically updates each time the RFID location data for that enterprise asset changes. In addition, the **Status** of the enterprise asset changes from **New** to **Matched** in the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table.
-   If a corresponding asset record does not already exist, data for that enterprise asset cannot be mapped from the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table to the Asset \[alm\_asset\] table. The **Status** of the enterprise asset changes from **New** to **Unmatched** in the RFID Asset \[sn\_itam\_common\_rfid\_asset\] table.

    You can view and take action on these unmatched enterprise assets by using the **Unmatched RFID tags** important action that appears on the **Overview** tab of the Enterprise asset estate view. For more information on the Enterprise asset estate view, see [Enterprise asset estate overview for Enterprise Asset Workspace](asset-estate-overview-eam.md).


You can view your asset records in the [Enterprise asset estate view](asset-estate-overview-eam.md) of the Enterprise Asset Workspace. For details on the RFID fields that are included in each asset record, see [Asset fields for enterprise assets](../reference/asset-fields-eam.md).

**Note:** If you are importing RFID location data for parent enterprise assets with one or more child enterprise assets, RFID location data for those child enterprise assets is based on the RFID tags that they are associated with.

-   If a child enterprise asset contains an RFID tag, RFID location data for that asset is based on that RFID tag.
-   If a child enterprise asset does not contain an RFID tag, RFID location data for that asset is based on the RFID tag of the parent enterprise asset. If you remove the parent enterprise asset, all RFID location data is cleared for the child enterprise asset.

