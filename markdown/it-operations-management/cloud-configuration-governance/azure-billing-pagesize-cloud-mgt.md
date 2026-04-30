---
title: Configure the download size of Microsoft Azure billing data
description: A single set of cloud billing data can be large. The MID Server, therefore, sends the data to the ECC queue in manageable chunks. You can optionally configure a system property to limit the size of each chunk to avoid performance issues caused by large data transfers.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create Microsoft Azure credentials for billing download, Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure the download size of Microsoft Azure billing data

A single set of cloud billing data can be large. The MID Server, therefore, sends the data to the ECC queue in manageable chunks. You can optionally configure a system property to limit the size of each chunk to avoid performance issues caused by large data transfers.

## Before you begin

Role required: admin

## Procedure

1.  Open the System properties table by entering `sys_properties.list` in the application filter.

2.  Filter the list to open the `sn_cmp.billing.page_size` property.

    The default value is 3 MB.

3.  Modify the value as needed.

    The maximum is 5 MB.

4.  Save the property.


