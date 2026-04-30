---
title: Create an OT discovered subnet
description: Create an Operational Technology \(OT\) discovered subnet to use during OT subnet mapping to help identify OT devices and assign them to the correct equipment model entity.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-02-10"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Create an OT discovered subnet

Create an Operational Technology \(OT\) discovered subnet to use during OT subnet mapping to help identify OT devices and assign them to the correct equipment model entity.

## Before you begin

Role required: cmdb\_ot\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Discovered Subnets**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |CIDR|Classless Inter-Domain Range \(CIDR\) to identify IP addresses for the discovered subnet.|
    |Discovered Managed Network|Name of the discovered managed network that the OT device belongs to.|
    |Site|Site that the OT device belongs to.|

    **Note:** The combination of CIDR, Discovered Managed Network, and Site should always be unique so that the OT devices are correctly mapped to the equipment model entities.

4.  Select **Submit**.

5.  To edit the discovered subnet record, open the record, make the changes as needed, and select **Update**.


**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](../../operational-technology-management/task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)

