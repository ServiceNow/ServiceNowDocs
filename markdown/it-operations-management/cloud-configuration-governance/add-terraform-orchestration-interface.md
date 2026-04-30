---
title: Add Terraform Orchestration interface on a resource block
description: After you have activated the Terraform store app for Cloud Provisioning and Governance, to support cloud-based operations for cloud providers using Terraform Open Source Edition. Add the Terraform Orchestration interface on resource block, to execute cloud-based operations via terraform templates.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add Terraform Orchestration interface on a resource block

After you have activated the Terraform store app for Cloud Provisioning and Governance, to support cloud-based operations for cloud providers using Terraform Open Source Edition. Add the Terraform Orchestration interface on resource block, to execute cloud-based operations via terraform templates.

## Before you begin

Role required: sn\_cmp.cmp\_root\_admin, sn\_cmp.cloud\_service\_designer

## Procedure

1.  On the Cloud Admin portal, navigate to **Design** &gt; **Resource Block**.

2.  Click the resource block, for example **Azure Datacenter**.

3.  Move the state of the resource block from **Published** to **Draft** to make it editable.

4.  Navigate to **General Information** &gt; **Guest Interface**, and then click **New**.

5.  Search for and select the **Terraform Orchestration Interface** from the Guest Interface list, and click **Submit**.

6.  Click the **Operations** tab.

7.  In the **Input Parameters**tab, navigate to **Interface** and select **Terraform Orchestration Interface**

8.  On the **Input Parameters** tab, configure the CAPI operation inputs.

    On the CAPI interface, which in this case is **Terraform Orchestration Interface**, open CreateStack method. The inputs from CAPI display on the Input tab, where you create parameters.

    The **Input Parameters** tab is where users enter values. You can map those input parameters to the parameters on the **Input** tab. To do this, copy the **Mapping** value from the **Input Parameters** tab into the **Value** field on the **Steps** &gt; **Input** tab.

    If this step is invoking a script, and that script requires arguments to return values, you can add a new input parameter for each argument. Use this syntax in the **Value** field: `${parameter.arg1}`.

9.  Click the **Steps** sub-tab under **Operations**.

10. Click **Add Step**.

11. Fill in the form fields.

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

API Provider

</td><td>

Select the API that provides the interfaces you need. The providers are part of the Cloud API \(CAPI\).

 For example, CAPI supplies the **Terraform OpenSource**provider, which provides the **Configuration Orchestration Interface**.

 This value appears if you select the Invoke Cloud API operation type.

</td></tr><tr><td>

API Interface

</td><td>

Select the interface that has the methods you want to use. For this example, the **Configuration Orchestration Interface** provides multiple interfaces or methods, which the system uses during provisioning.

</td></tr><tr><td>

API Method

</td><td>

Select the method to perform the operation. In this example, **ExecuteCommand** is required to provision terraform templates.

</td></tr><tr><td>

CAPI Version

</td><td>

Enter the version of the CAPI API.

</td></tr><tr><td>

Condition

</td><td>

Enter an optional condition that must be met before the system uses this step.

</td></tr></tbody>
</table>12. Click **Submit**.

    The **Input** and **Response Processor** tabs appear for the step.

13. On the **Input** tab, configure the CAPI operation inputs.

    On the CAPI interface, which in this case is **Configuration Orchestration Interface**, open ExecuteCommand method. The inputs from CAPI show on the Input tab, where you create parameters.

    Remember that the parameters on the **Input Parameters** tab is where users enter values. You can map those input parameters to the parameters on the **Input** tab. Copy the **Mapping** value from the **Input Parameters** tab into the **Value** field on the **Steps** &gt; **Input** tab.

    If this step is invoking a script, and that script requires arguments to return values, you can add a new input parameter for each argument. Use this syntax in the **Value** field: `${parameter.arg1}`.

    **Note:** Map the values as mentioned in the following table for the following parameters:

<table id="table_kr1_4fz_kjb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

AdditionalParameters

</td><td>

Enter the following script: ```
{"ServerType":"$(Script:sn_cmp_terraform.TerraformCommandUtils.
getConfigProviderServerTypeByName[arg=${parameter.WorkloadConfigProvider}])"}
```

</td></tr><tr><td>

ConfigMgmtProviderInfo

</td><td>

```
$(capiResolver.NodeCredentialResolver#nodeCredentialId=$(ci.sn_cmp_wl_cfg_mgmt_provider
[name=${parameter.WorkloadConfigProvider}].credential))
```

</td></tr><tr><td>

Node Address

</td><td>

```
$(ci.cmdb_ci_workload_config_provider[name=${parameter.WorkloadConfigProvider}].url)
```

</td></tr><tr><td>

Script For CreateStack operation

</td><td>

```
${CloudScript.scripts.TerraformDeploy}
```

</td></tr><tr><td>

ScriptFor DeleteStack operation

</td><td>

```
${CloudScript.scripts.DestroyTerraform}
```

</td></tr></tbody>
</table>14. On the **Response Processor** tab, configure the response processors by attaching resource scripts.

    You would have added Resource Scripts to the resource block, while creating the Resource Block.

15. From the Operation list, select the **CreateStack** or **DeleteStack** operation.

16. Click the add icon![Add Response Processor](../image/add-button.png)for **Add Response Processor**.

17. Click the **Resource Script** sub tab, and then click **New**.

18. Complete the form.

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
</table>19. From the **Script Name** list, select the script corresponding to the selected operation, and click **Submit**.

20. Move the state of the resource block from **Draft** to **Published**.

    The datacenter resource block moves from the draft to the published state and you cannot make further changes to the resource block. You can only modify a resource block after you set the status to **Draft**.


**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

