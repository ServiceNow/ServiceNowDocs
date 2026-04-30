---
title: View OT devices not assigned to a site
description: View the list of Operational Technology \(OT\) devices that aren't assigned to a site.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# View OT devices not assigned to a site

View the list of Operational Technology \(OT\) devices that aren't assigned to a site.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: cmdb\_ot\_isa\_editor and cmdb\_ot\_editor

## About this task

As part of OT device mapping, you need to assign the device to a site before mapping it to an equipment model entity. To do this, you can view a list of all the OT devices that aren't assigned to a site.

## Procedure

1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **OT Devices w/o Site Assignment**.

2.  To assign a device to a site individually, select the device record and updating the **Site** field.

3.  To perform a bulk edit to update the **Site** column and assign multiple devices to the same site, complete the following steps.

    1.  Select the check boxes next to each OT device you want to assign to a site.
    2.  In the **Site** column header, select the Column options button and choose **Update Selected**.
    3.  Update the **Site** field.
    4.  Select **Update**.

## What to do next

The OT devices are assigned to a site but not mapped to an equipment model entity. You can view a list of the unmapped OT devices to complete the device mapping. For more information, see [View unmapped OT devices](view-unmapped-ot-devices.md).

**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](automate-mappings-between-ot-assets-and-equipment-model-entity.md)

