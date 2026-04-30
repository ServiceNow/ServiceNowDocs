---
title: Asset and Configuration Item \(CI\) synchronization for Operational Technology \(OT\) assets
description: Maintain synchronization between asset and CI for OT assets through MAC address on the asset and the Network Adapter CI.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [OT Asset Management, Explore, Enterprise Asset Management, IT Asset Management]
---

# Asset and Configuration Item \(CI\) synchronization for Operational Technology \(OT\) assets

Maintain synchronization between asset and CI for OT assets through MAC address on the asset and the Network Adapter CI.

Synchronization between asset and CI is achieved using the **Serial number** field. However, an OT asset need not necessarily have a serial number, but it’s associated with a MAC address. Therefore, the asset-CI synchronization for OT assets includes the **MAC address** \(mac\_addr\) field in the Asset \[alm\_asset\] table in addition to the serial number.

A CI can have multiple MAC addresses. The Network Adapter \[cmdb\_ci\_network\_adapter\] table stores all the MAC addresses and also has a reference field to the CI \[cmdb\_ci\] table. Therefore, the relationship between MAC address and CI is maintained.

## Synchronization from asset to CI

When an asset is created with a MAC address, synchronization happens as follows:

1.  A CI is created.
2.  A record for the corresponding MAC address is created in the Network Adapter \[cmdb\_ci\_network\_adapter\] table with a reference to the CI.

When the MAC address of an asset is updated, the existing record in the Network Adapter \[cmdb\_ci\_network\_adapter\] table isn't updated. Instead, a new record is created in the Network Adapter \[cmdb\_ci\_network\_adapter\] table.

## Synchronization from CI to asset

When a CI is created with a MAC address, synchronization happens as follows:

1.  An asset is created.
2.  The MAC address of the CI is copied to the asset.

If there's an existing CI, then the associated asset is updated with the MAC address only if the asset doesn't have it already.

## Rules for generating CI names

A CI name follows a format that's based on the following conditions:

|Condition|CI name format|
|---------|--------------|
|Asset has a Serial number|Concatenation of Serial number and Model name separated by hyphen. For example, SN123 - DemoModel.|
|Asset has a Serial number and a MAC address|Concatenation of Serial number and Model name separated by hyphen. For example, SN123 - DemoModel.|
|Asset has no Serial number but has a MAC address|Concatenation of MAC address and Model name separated by hyphen. For example, 88-22-33-66-888-AB - DemoModel.|
|Asset has no Serial number and MAC address|Model name|

Whenever there are updates to **Serial number** or **MAC address** fields, the CI name is synchronized only under the following conditions:

-   CI name isn't updated manually.
-   The Discovery source is **SNassetmanagement**, which means that the CI is created from an asset.
-   CI name hasn't been modified by CMDB.

**Note:** The **sn\_itam\_common.mac\_address\_sync** system property enables you to synchronize asset and CI using the Mac address. By default, this system property is set to **false**. To enable synchronization through the Mac address, set this system property to **true** by navigating to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Other configuration**.

## OT entity synchronization between asset and CI

The CI \[cmdb\_ci\] table has the **OT entity** \[cmdb\_ot\_entity\] field. Also, the Asset \[alm\_asset\] has a corresponding **OT entity** \[ot\_entity\] field. Synchronization of the OT entity happens as follows:

-   When a CI is created with the OT entity reference set on the CI, the **OT entity** \[ot\_entity\] field in the Asset \[alm\_asset\] table is set to **true**.
-   When an asset with the OT entity set to **true** is created, a corresponding CI and an OT entity are created on the CMDB side. The OT entity reference is then set on the CI.

**Important:** After a CI is marked as an OT entity, it can't be reverted to a non-OT entity.

**Parent Topic:**[OT Asset Management](ot-asset-management.md)

**Related topics**  


[OT Asset Management licensing](licensing-ot-asset-management.md)

[View the license report for the OT Asset Management application](../task/view-license-report-otam.md)

[OT Asset Workspace](ot-asset-ws-otam.md)

