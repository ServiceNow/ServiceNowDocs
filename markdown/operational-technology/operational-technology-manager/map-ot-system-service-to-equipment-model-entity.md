---
title: Map an Operational Technology system service to an equipment model entity
description: Map an Operational Technology \(OT\) system service to an ISA equipment model entity by enabling a scheduled job. When the relationship between an OT device and an equipment model entity changes, the scheduled job recomputes the relationship between the OT system service and the equipment model entity.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Modeling an Operational Technology system service, Use, Operational Technology Manager, Operational Technology]
---

# Map an Operational Technology system service to an equipment model entity

Map an Operational Technology \(OT\) system service to an ISA equipment model entity by enabling a scheduled job. When the relationship between an OT device and an equipment model entity changes, the scheduled job recomputes the relationship between the OT system service and the equipment model entity.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select the Show/hide filter \(![Show/hide filter icon in the table header.](../image/show-hide-filter-icon.png)\) icon.

3.  Add the following filter.

    `[Name] [is] [Map OT Systems to ISA Entities]`

4.  Select the **Map OT Systems to ISA Entities** scheduled job record.

5.  Next to the **Active** field, select the check box.

6.  In the **Run** field, select the option that best fits your needs.

7.  Select **Update**.


**Parent Topic:**[Modeling an Operational Technology system service](../concept/modeling-ot-system.md)

