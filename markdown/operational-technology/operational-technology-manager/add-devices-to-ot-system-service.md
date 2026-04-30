---
title: Add a device to an Operational Technology system service
description: Add an Operational Technology \(OT\) device to an OT system service to create a relationship between the equipment model entity that the device belongs to and the OT system service.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Modeling an Operational Technology system service, Use, Operational Technology Manager, Operational Technology]
---

# Add a device to an Operational Technology system service

Add an Operational Technology \(OT\) device to an OT system service to create a relationship between the equipment model entity that the device belongs to and the OT system service.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the List \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the **Operational Technology \(OT\)** module, select the **OT Systems** list.

4.  Select the OT system service you want to add a device to.

5.  In the **Related Records** tab, select the **Associated OT Devices** related record.

6.  Select **Add**.

7.  Select the check box next to one or more OT devices.

8.  After you choose all the OT devices, select **Add**.


## Result

After you add the OT devices, the following relationships are created:

-   The Depends on::Used by relationship between the selected configuration item \(CI\) and the OT system service
-   The Managed by::Manages relationship between the OT system service and CI's equipment model entity.

**Parent Topic:**[Modeling an Operational Technology system service](../concept/modeling-ot-system.md)

