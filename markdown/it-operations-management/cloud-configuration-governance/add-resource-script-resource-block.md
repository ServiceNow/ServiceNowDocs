---
title: Add a resource script to a resource block
description: A resource script operates on a resource during deployment or returns data to the CMDB after a resource is deployed.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Add a resource script to a resource block

A resource script operates on a resource during deployment or returns data to the CMDB after a resource is deployed.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Open the resource block and then set it to **Draft** ![Draft .](../image/draft-published-slider.png) state.

3.  On the **Resource Script** tab, specify a unique and meaningful **Name** and then define the script:

<table id="table_wqf_ygs_vz"><tbody><tr><td>

Script

</td><td>

Script code.

</td></tr><tr><td>

Type

</td><td>

Type of script:-   Instance Script: Javascript that performs an operation on the instance \(for example, a subflow\).
-   PowerShell Script
-   Python Script
-   Response Processor: Converts return data from the external cloud API to the operation implementation into a format that the CMDB can accept.
-   Shell Script


</td></tr></tbody>
</table>4.  Click **Submit**.

    Add as many scripts as are needed.


**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

