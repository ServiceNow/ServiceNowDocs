---
title: Preview existing OT records in the CMDB
description: Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validate imported staging records, Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Preview existing OT records in the CMDB

Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.

## Before you begin

Role required: ot\_excel\_import\_user

## About this task

If a matching configuration item \(CI\) is in the CMDB when you import OT devices from the staging table, existing records may reconcile or merge with new records. Matching CIs include the hostname, MAC address, or serial number. To avoid accidentally reconciling or merging records, you can preview the existing records that share the matching CIs with the records in the staging table.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the OT Excel SGC - Import Task module, select one of the available lists.

4.  Select an Import Task record that you want to verify has any matching CIs.

5.  In the Validation comments column, check if a matching CI has been found.

    The Validation comments column explains the matching CI that was found and contains a link to the matching CI. When a matching CI is found in the CMDB, the Validation state is set to **Partially Valid**. The following table lists the matching CI validation comments.

    |Matching CI|Validation comment|
    |-----------|------------------|
    |Hostname|Same transformed name found for another CI:&lt;Link to CI&gt;|
    |MAC address|Same MAC address \[MAC address\] found for another CI:&lt;Link to CI&gt;|
    |Serial number|Same serial number \[serial number\] found for another CI: &lt;Link to CI&gt;|

6.  View the matching CI by selecting it from the Matching CI in the CMDB column.


**Parent Topic:**[Validate imported staging records](run-validations.md)

