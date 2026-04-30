---
title: Enable Nutanix v4 discovery
description: Enable Nutanix v4 discovery by setting the MID Server property value to the exact v4 version.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-10-12"
reading_time_minutes: 1
breadcrumb: [Nutanix Acropolis, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable Nutanix v4 discovery

Enable Nutanix v4 discovery by setting the MID Server property value to the exact v4 version.

## Before you begin

Verify that you have Discovery and Service Mapping Patterns installed \(starting with version 1.29.0\).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for the `sn_itom_pattern.nutanix_prism_version` property.

3.  Select the **sn\_itom\_pattern.nutanix\_prism\_version** property.

4.  In the **Value** field, enter the exact v4 version to discover.

    For example: `v4.0.b1`.

5.  Select **Update**.


**Parent Topic:**[Nutanix Acropolis discovery](../reference/nutanix-pattern.md)

