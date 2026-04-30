---
title: Validate legacy IBM PVU Process Pack requirements for associating software installations with PVU mappings
description: Meet the recommended requirements to ensure that you receive the highest quality results with PVU mapping.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Validate legacy IBM PVU Process Pack requirements for associating software installations with PVU mappings

Meet the recommended requirements to ensure that you receive the highest quality results with PVU mapping.

## Before you begin

Role required: admin

## Procedure

1.  Use a discovery tool, such as ServiceNow Discovery, to identify hardware and populate the configuration management database \(CMDB\) with the configuration items you want to manage with IBM PVU licensing.

2.  Use a discovery tool, such as ServiceNow Discovery, to identify software installations.

    Check that the added CPU information is correct.

3.  [Activate](t_ActivatingTheIBMPVUProcessPack.md) the Software Asset Management plugin - IBM PVU Process Pack plugin.

    This also activates the Software Asset Management plugin if it is not already active.

4.  [Refresh processor definitions.](t_RefreshProcessorDefinitions.md)

5.  Ensure that the [software models](t_ManagingSoftwareModels.md) you want to manage with IBM PVU licensing have the correct license type: **Per installation - IBM PVU**.

6.  [Create software counters](t_UseSWCountersCalcIBMPVULice.md) to calculate IBM PVU licenses.

7.  Count licenses to determine compliance with IBM PVU guidelines.


**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

