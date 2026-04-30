---
title: Configure endpoint operation mapping
description: You can configure endpoint mapping on a storage volume to make a connection to a resource.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Create a custom resource block, Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure endpoint operation mapping

You can configure endpoint mapping on a storage volume to make a connection to a resource.

## Before you begin

Role required: admin

## About this task

In the following example, the endpoint mapping that is configured for a storage volume specifies the conditions that must be met and the operation to execute to make a connection to a resource \(a virtual server in the example\) that supports a binding interface to a storage volume. The storage volume implements the endpoint \(type Block EP in the example\) and the virtual server consumes the endpoint:

![Endpoint mapping for a storage volume](../image/connection-in-blueprint-canvas.png "Endpoint mapping for a storage volume")

The settings on the example **Resource Endpoint Mappings** related list specifies the conditions and an action:

-   For a resource block that supports a binding interface to a **Storage Volume**
-   For a **Source** resource with **CI type** of **Storage Volume**
-   With an **Endpoint** type of **Block EP** \(cmdb\_ci\_endpoint\_block\)

Use the **Attach** operation to implement the connection. Use the specified **Operation Implementation** to perform the **Attach** operation.

![Storage volume for a resource block](../image/endpoint-mapping-rel-list.png "Storage volume for a resource block")

## Procedure

1.  While configuring a resource block, open the **Resource Endpoint Mapping** related list, click **New**, and then specify the following settings:

<table id="table_ipj_nfn_5z"><tbody><tr><td>

Binding Resource

</td><td>

Resource block that consumes the **Endpoint** that the **Source Resource** presents.

</td></tr><tr><td>

Endpoint

</td><td>

Type of endpoint that the **Source Resource** presents.

</td></tr><tr><td>

Type

</td><td>

Type of operation to perform for the mapping. Only operations that are appropriate for the specified **Endpoint** appear in the list.

</td></tr><tr><td>

Operation implementation

</td><td>

Implementation that is called to perform the operation that you are defining in this mapping.

</td></tr><tr><td>

Application

</td><td>

Read-only. Cloud Provisioning and Governance application.

</td></tr><tr><td>

Source Resource

</td><td>

Resource block that can present an **Endpoint** of the type that you specified. You typically do not change this setting.

</td></tr></tbody>
</table>2.  Repeat the process for as many mappings as are needed.


**Parent Topic:**[Create a custom resource block](create-resource-block.md)

**Related topics**  


[Specify a host resource for a resource block](specify-host-resource-cmp.md)

[Specify the bindings for resource blocks](specify-resource-bindings-cmp.md)

