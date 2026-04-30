---
title: Validate legacy Oracle Process Pack requirements for associating software installations with Oracle mappings
description: Meet the recommended requirements to ensure that you receive the highest quality results with Oracle mapping.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Legacy Oracle process pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Validate legacy Oracle Process Pack requirements for associating software installations with Oracle mappings

Meet the recommended requirements to ensure that you receive the highest quality results with Oracle mapping.

## Before you begin

Role required: admin

## Procedure

1.  Use a discovery tool \(such as ServiceNow Discovery\) to identify software installations.

    Check that the added CPU information is correct.

2.  [Activate](t_ActivateSWAssetMgmtOraclProcPac.md) the legacy Software Asset Management - Oracle Process Pack \(com.snc.sam.oracle.pp\) plugin.

    This also activates the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin if it is not already active.

3.  Refresh processor definitions by navigating to **Software Asset** &gt; **System** and clicking **Refresh Processor Definitions**.

4.  Ensure that the software models that you want to manage with Oracle licensing are set up accurately.

    See [Creating a software model](t_ManagingSoftwareModels.md).

5.  [Create a software license](t_CreateAnOracleSoftwareLicense.md) for your Oracle software.

    Ensure that the license is given the correct license metric.

    The **License metric** \(metric\_type\) field on the Software License table is a reference field to the License Calculation table.

6.  [Create a software counter](../concept/c_CreatingAnOracleSoftwareCounter.md) to calculate Oracle licenses with the matching license type.

7.  Count licenses to determine compliance with Oracle guidelines.


**Parent Topic:**[Legacy Oracle process pack](../concept/c_OracleProcessPack.md)

