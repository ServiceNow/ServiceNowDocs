---
title: Specify the bindings for resource blocks
description: Bindings represent endpoint relationships. For example, a storage volume might implement an endpoint type of Block EP \(cmdb\_ci\_endpoint\_block\). A virtual server might consume an endpoint of that type. Bindings must support the Guest interface that is specified for the resource block.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Create a custom resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Specify the bindings for resource blocks

Bindings represent endpoint relationships. For example, a storage volume might implement an endpoint type of Block EP \(cmdb\_ci\_endpoint\_block\). A virtual server might consume an endpoint of that type. Bindings must support the Guest interface that is specified for the resource block.

## Before you begin

Role required: admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Select the resource block and then select **Draft** on the **Resource Blocks** form: ![Draft.](../image/draft-published-slider.png)

3.  In the **Resource Bindings** related list, click **New**.

4.  On the **Resource Binding** form, the **Application** and the **Guest Resource** \(the resource block that you are currently configuring\) are already specified.

    Specify the **Binding Resource**.

5.  Click **Submit**.


**Parent Topic:**[Create a custom resource block](create-resource-block.md)

**Related topics**  


[Specify a host resource for a resource block](specify-host-resource-cmp.md)

[Configure endpoint operation mapping](configure-endpoint-mapping-cmp.md)

