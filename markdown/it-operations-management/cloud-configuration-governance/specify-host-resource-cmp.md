---
title: Specify a host resource for a resource block
description: Hosts that support the Host interface of a resource block are potential hosts for the resource block. You use the Host interface setting to further limit the options that are presented to the stack requester while selecting a host type.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Create a custom resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Specify a host resource for a resource block

Hosts that support the **Host interface** of a resource block are potential hosts for the resource block. You use the **Host interface** setting to further limit the options that are presented to the stack requester while selecting a host type.

## Before you begin

Role required: admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Select the resource block and then select **Draft** on the **Resource Blocks** form: ![Draft.](../image/draft-published-slider.png)

3.  In the **Host Resource** related list, click **New**.

    On the **Resource Host** form, the **Application** and the **Guest Resource** \(the resource block that you are currently configuring\) are already specified.

4.  Specify the **Host Resource**.

    For example, for a virtual server, you might select **AWS Datacenter** or **Azure Datacenter** as potential host types.

5.  Click **Submit**.


**Parent Topic:**[Create a custom resource block](create-resource-block.md)

**Related topics**  


[Specify the bindings for resource blocks](specify-resource-bindings-cmp.md)

[Configure endpoint operation mapping](configure-endpoint-mapping-cmp.md)

