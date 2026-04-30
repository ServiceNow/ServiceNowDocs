---
title: Create an action for an 'on Resource operation' policy
description: The on Resource operation trigger fires during the Orchestration process when a user performs a Start, Stop, or Deprovision life cycle operation on a specific resource. A policy that is triggered by the on Resource operation trigger can override a user-requested attribute value, run a script, call a Cloud API, or perform an IP address management operation.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an action for an 'on Resource operation' policy

The on Resource operation trigger fires during the Orchestration process when a user performs a Start, Stop, or Deprovision life cycle operation on a specific resource. A policy that is triggered by the on Resource operation trigger can override a user-requested attribute value, run a script, call a Cloud API, or perform an IP address management operation.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor or admin
-   Optional: [Create one or more cloud policy groups](create-cloud-policy-group.md).
-   [Configure a cloud policy rule](configure-cloud-policy-rule.md) and associated conditions.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform, enter a unique and meaningful **Action Name**, and then fill in the form for the action.

    ![Create Action popup](../image/action-on-resource-operation.png)

<table id="table_qhx_32h_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property

</td><td>

Specify the name of the property \(attribute\) on the user request form to override.

</td></tr><tr><td>

Value

</td><td>

Enter a value that overrides the value in the **Property** field. You can override text values only. You can specify a static value, an expression, or both. The example action, named **SetTheCostCenter**, specifies the value **Marketing** for the **CostCenter** property.

![Configure a Property Override action](../image/action-property-override.png "Configure a Property Override action")

**Note:**

When both a policy rule and a form rule overwrite a value, the value in the form rule is used.

Expressions can perform the following actions \(see [Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt-1.md) for details\):

-   Set form data values using definition expressions. For example: `${parameter.formData.CatalogAttributeType}`
-   Assign user data values using definition expressions. For example: `${parameter.userData.userId}`

For example, the following value can set the stack name to **Stack\_Bob.Smith@company.com**: `Stack_${parameter.userData.userId}`

-   Set stack or table values using runtime expressions.

For example: `$(ci.sn_cmp_ip_pool[subnet=${parameter.formData.Subnet Id}])` takes the subnet from the IP Pools table.

-   Associate a random number with a field using static expressions. Use: `${randomNumber}`


</td></tr><tr><td>

Is Script Based

</td><td>

Select the check box to display the **Script** text box and then specify the script.You can use the following example script snippet to override a stack name. The `function( formData)` section of the script modifies the values for fields on the form. `MyStack` is the stack name in this example.

 ```
customScript : function( formData){
               // Manipulation of form parameter is only supported here. 
               // Change in any other attributes will be ignored
               // data available for manipulation are
               // Form Data - Ex. StackName can be accessed 
               // through formData.StackName
               // formData.StackName = "MyStack";
               // User Data - Ex. User Id can be accessed 
               // through this.parameters.userData
               // if(this.parameter.userData.userId == 'servicenowuserId')
                  formData.StackName = "MyStack";
                  return formData;
                },

```

</td></tr></tbody>
</table><table id="table_nbq_j2h_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Script Category

</td><td>

Select a category.

</td></tr><tr><td>

Action Script Name

</td><td>

Specify a unique and meaningful name for the script.

</td></tr><tr><td>

Action Script

</td><td>

Create the script in the text box.See [Create a policy action script](create-policy-script-1.md) for details.

</td></tr></tbody>
</table>    If you select the **Call Cloud API** action type and save the record, the Policy Rule Action Attributes related list is populated with the attributes to pass to the provider. If you are integrating with Infoblox, you must configure the **DNSSuffix** field. When you create a host, for example, the value in the **DNSSuffix** field appears in Infoblox for the newly created virtual machine.

<table id="table_pmz_12p_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Name

</td><td>

Enter a descriptive name for the action. In subsequent policy actions for the same policy, you can reference this name in a **Value** field. It refers to the JSON payload that is received from the cloud provider after an API call. For example, to reference an allocated IP address that was returned by the action that is named RefAction, you can use the following expression in the **Value** field of another policy action: `$(parameter.RefAction.Allocated_IP}`.

</td></tr><tr><td>

Provider

</td><td>

Enter the cloud provider from the API library.

</td></tr><tr><td>

Version

</td><td>

Enter the version from the API library.

</td></tr><tr><td>

Interface

</td><td>

Select a CAPI interface. For Infoblox, select **IPAM interface**.

</td></tr><tr><td>

Operation

</td><td>

Select a CAPI interface operation to perform. For Infoblox, select **CreateHostRecord** or **DeleteHostRecord**.

</td></tr><tr><td>

Credentials

</td><td>

Enter the sys\_ID of the necessary credentials. You can also use an expression like:

```
$(ci.sn_cmp_infoblox_server[$(ci.sn_cmp_ip_pool[subnet=${parameter.formData.SubnetId}].provider_instance)].infoblox_server_credential)
```

</td></tr><tr><td>

Endpoint URL

</td><td>

Enter the endpoint URL of the connector from the API library. For Infoblox, it is the IP address of the Infoblox server.

</td></tr></tbody>
</table><table id="table_ncj_b2p_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IPAM Method Name

</td><td>

Select the IPAM Method Name. For Infoblox, select one of the following options: -   **Release IP Address**: Release an IP address from Infoblox when a machine is deprovisioned.
-   **Register IP Address**: Register a new virtual machine to Infoblox. This option is used by AWS and Azure clouds.
-   **Reserve IP Address**: Reserve a new IP address. This option is used by a vSphere cloud.
 See [Register IP addresses for AWS and Azure virtual machines in Infoblox](register-ip-address-aws-azure.md), [Reserve IP addresses for VMware vSphere virtual machines in InfoBlox](reserve-ipaddress-vmware.md), and [IPAM integration](../concept/IPAM-integration.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Create a cloud policy](create-cloud-policy.md)

