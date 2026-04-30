---
title: Create a resource block for Microsoft Azure Cloud
description: Resource blocks are the building blocks of cloud catalog items. Create a resource block for the Microsoft Azure Cloud Platform provider, based on a CI type from the CMDB.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a resource block for Microsoft Azure Cloud

Resource blocks are the building blocks of cloud catalog items. Create a resource block for the Microsoft Azure Cloud Platform provider, based on a CI type from the CMDB.

## Before you begin

Role required: sn\_cmp.cmp\_root\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

2.  Click **New** to open the Create Resource Block dialog box and then fill in the form.

    For a detailed description of each field, see [Create a custom resource block](create-resource-block.md).

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name \(**Azure Datacenter**\) for the resource block.|
    |Description|Enter a valid description|
    |Layer|Select the type of resource block \(**Logical Datacenter**\).|
    |CI Type|Select the CI type \(**Azure Datacenter**\) that the resource block represents.|
    |Guest Interface|Select a default guest interface \(**Compute Interface**\) to use when you add a resource block to a template.|

3.  Click **Submit**.

    The resource block information appears.

4.  Click the **Resource Script** sub tab and then click **New**.

<table id="table_hwh_cw2_pdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name \(For example, **Create\_AzureTF\_Stack\_Response\_Processor**\) for the resource script.

</td></tr><tr><td>

Type

</td><td>

Select a type \(**Response Processor**\) for the script.

</td></tr><tr><td>

Script Resource Script for Create

</td><td>

Enter the following script: ```
function processResponse (response, cloudServiceAccountId, ldc,
						  correlationId, step, requestorContext, stackId) {
	var responseObject = global.JSON.parse(response);
	var tfState = global.JSON.parse(responseObject.terraform.state);
	var processor = new sn_cmp_terraform.TerraformResponseProcessor();
	var processedResponses = processor.processResponse(tfState, cloudServiceAccountId,  ldc,
							   correlationId, step, requestorContext, stackId);
	return global.JSON.stringify(processedResponses);
}

```

</td></tr><tr><td>

Script Resource Script for Delete

</td><td>

Enter the following script: ```
function processResponse (response, cloudServiceAccountId, ldc,
						  correlationId, step, requestorContext, stackId) {
	var responseObject = global.JSON.parse(response);
	var tfState = global.JSON.parse(responseObject.terraform.state);
	var processor = new sn_cmp_terraform.TerraformResponseProcessor();
	var processedResponses = processor.processResponse(tfState, cloudServiceAccountId,  ldc,
							   correlationId, step, requestorContext, stackId);
	return global.JSON.stringify(processedResponses);
}

```

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  Click the **Operations** sub tab and then click **Steps**.

7.  Select **CreateStack** from the **Operations** list.

8.  Click the **Add a Step** plus icon to open the Add Operation Steps dialog box and then fill in the form.

<table id="table_q1n_4qw_52b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation Type

</td><td>

Select the type of operation.

 **Invoke Cloud API**: Select this option to select a provider, interface, and method from CAPI.

</td></tr><tr><td>

API Provider\[Operation Type = Invoke Cloud API\]

</td><td>

Select the API that provides the interfaces you need. The providers are part of the Cloud API \(CAPI\).

 For example, CAPI supplies the **Terraform OpenSource**provider, which provides the **Configuration Orchestration Interface**.

 This value appears if you select the Invoke Cloud API operation type.

</td></tr><tr><td>

API Interface\[Operation Type = Invoke Cloud API\]

</td><td>

Select the interface that has the methods you want to use. For this example, the **Configuration Orchestration Interface** provides multiple interfaces or methods, which the system uses during provisioning.

</td></tr><tr><td>

API Method\[Operation Type = Invoke Cloud API\]

</td><td>

Select the method to perform the operation. In this example, **ExecuteCommand** is required to provision terraform templates.

</td></tr><tr><td>

CAPI Version\[Operation Type = Invoke Cloud API\]

</td><td>

Enter the version of the CAPI API.

</td></tr><tr><td>

Condition

</td><td>

Enter an optional condition that must be met before the system uses this step.

</td></tr></tbody>
</table>9.  Click **Submit**.

10. Click **Response Processor** and then click the plus icon.

    The Add Response Processor dialog box appears.

11. Select **Create\_AzureTF\_Stack\_Response\_Processor** from the **Script Name** list and click **Submit**.

12. Move the state of the resource block from **Draft** to **Published**.

    The Azure Datacenter resource block moves from the draft to the published state and no further changes can be made to the resource block. Changes to a resource block can be made only if the status is set to **Draft**.


**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

