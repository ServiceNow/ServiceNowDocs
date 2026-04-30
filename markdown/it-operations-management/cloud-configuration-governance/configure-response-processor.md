---
title: Configure a response processor
description: Configure a response processor to handle responses from datacenters.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure a response processor

Configure a response processor to handle responses from datacenters.

## Before you begin

-   The CI class types for your resources must already exist in the CMDB. If you created custom products or providers in CAPI, you must also create custom CI types so the response processor knows how to identify CIs. See [Create a CI class for a virtual cloud resource](create-a-ci-class-cloud.md) for information on creating CI types.

Role required: sn\_cmp.cloud\_service\_designer

## About this task

After each step is completed, the datacenter sends a response to the ECC Queue of the MID Server. For example, if a user provisions a virtual server on an AWS datacenter, AWS sends information about the new virtual server to the ECC Queue. The system needs to create a CI in the CMDB for the virtual server. It does this using a response processor.

Alternatively, you can use pattern-based targeted discovery to handle responses from the datacenters. For more information, see [Pattern-based targeted discovery](../concept/pattern-based-targeted-discovery.md#).

**Note:** The resource type for which you are adding the response processor script must exist in the \[sn\_capi\_resource\_type\] table.

## Procedure

1.  Open a resource block, and click the **Resource Script** tab.

    Ensure that the resource block is not in the published state.

2.  Click **New**.

3.  In the **Name** field, enter the name for the resource script.

4.  In the **Script** field, enter a script.

5.  Click **Submit**.

6.  Click the **Operations** tab on the resource block.

7.  Click the **Steps** sub tab.

8.  Click a step.

9.  Click the **Response Processor** tab for the step.

10. Click the add icon \(![Adding a response processor](../image/add-button.png)\).

11. In the **Script Name** field, select the processor you just created.

12. Click **Submit**.

    The response processor script can process the response from the cloud provider for the CI type of the resource block.


-   **[Execute response processor for workflow](create-response-processor.md)**  
Execute a response processor for a workflow to get the workflow data back into a configuration item \(CI\). The response processor picks up the data, sends the data to the CMDB which in turn puts the data in a CI.
-   **[Virtual server response processor example](../reference/response-processor-example.md)**  
The **Create\_Virtual\_Server\_Response\_Processor** script, which is available by default in Cloud Provisioning and Governance, is the response processor that handles the creation of AWS virtual machine CIs.

**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

