---
title: Create an action for an 'on Blueprint provision' policy
description: The on Blueprint provision trigger fires after execution of on Catalog item request start policies. A policy that is triggered by the on Blueprint provision trigger can run a script, override a user-requested attribute value, or abort and send a message about the provision operation.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an action for an 'on Blueprint provision' policy

The on Blueprint provision trigger fires after execution of on Catalog item request start policies. A policy that is triggered by the on Blueprint provision trigger can run a script, override a user-requested attribute value, or abort and send a message about the provision operation.

## Before you begin

Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).

[Configure a cloud policy rule](configure-cloud-policy-rule-1.md)

Role required: sn\_cmp.cloud\_governor or admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform, enter a unique and meaningful **Action Name**, and then fill in the form for the action.

    ![Create Action popup](../image/action-on-bp-prov-cloud-mgt.png)

<table id="table_nbq_j2h_sfb"><thead><tr><th>

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
</table><table id="table_qhx_32h_sfb"><thead><tr><th>

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
</table>    |Field|Description|
    |-----|-----------|
    |Message|Enter the message to present to the requester when the process aborts.|


