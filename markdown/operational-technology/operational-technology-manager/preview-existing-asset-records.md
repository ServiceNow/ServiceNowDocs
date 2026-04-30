---
title: Preview existing OT records in the CMDB
description: Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Preview existing OT records in the CMDB

Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.

## Before you begin

Role required: cmdb\_ot\_admin or admin

## About this task

If a matching configuration item \(CI\) is in the CMDB when you import OT devices from the staging table, existing records may reconcile or merge with new records. Matching CIs include the hostname, MAC address, or serial number. To avoid accidentally reconciling or merging records, you can preview the existing records that share the matching CIs with the records in the staging table.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager** &gt; **Import OT Devices - Staging Table**.

    The validation comments explain the matching CI that was found and contain a link to the matching CI. When a matching CI is found in the CMDB, the Validation state is set to **Partially Valid**. The following table lists the matching CI validation comments.

    |Matching CI|Validation comment|
    |-----------|------------------|
    |Hostname|Same transformed name found for another CI:&lt;Link to CI&gt;|
    |MAC address|Same MAC address \[MAC address\] found for another CI:&lt;Link to CI&gt;|
    |Serial number|Same serial number \[serial number\] found for another CI: &lt;Link to CI&gt;|

2.  View the matching CI by selecting it from the Matching CI in the CMDB column.


**Parent Topic:**[Configuring Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

