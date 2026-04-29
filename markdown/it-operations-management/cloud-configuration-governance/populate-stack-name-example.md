---
title: Populate stack name with a script
description: This example illustrates how to populate the name of the stack that a user requests from the Cloud Provisioning and Governance catalog by utilizing the user's ID. The example uses a script include that you can call from a blueprint rule action.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud catalog form configuration examples, Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Populate stack name with a script

This example illustrates how to populate the name of the stack that a user requests from the Cloud Provisioning and Governance catalog by utilizing the user's ID. The example uses a script include that you can call from a blueprint rule action.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

Before you can follow this example, you should be familiar with creating blueprints and blueprint rules. See these resources:

-   [Cloud Provisioning Blueprints](../concept/blueprints.md)
-   [Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)
-   [Configure a blueprint rule](configure-a-blueprint-rule.md#)

This example uses a script include. If you want to create similar script includes, familiarize yourself with the Glide System APIs that are part of your instance. See the [Developer site](https://developer.servicenow.com) for a comprehensive list of all APIs. See [Script Includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US) for more information about how the system uses these scripts.

## About this task

The goal of this example is to take the ID of the catalog requester and populate it in the Stack Name field. The field remains editable. Follow an example like this one when you want to loosely enforce a naming or labeling convention on certain values, but still allow the user to enter the text that they want.

## Procedure

1.  Create a script include that returns the user ID of the person requesting the catalog item:

    1.  In the standard interface for the instance \(not in the Cloud Admin Portal\), click the gear icon \(![System settings gear icon](../image/icon-gear-system-settings.png)\) in the upper left, and then click **Developer**.

    2.  In the **Application** field, select **Cloud Provisioning and Governance**.

        ![Changing the scope](../image/scope-cmp.png)

        The application scope of your instance changes to**Cloud Provisioning and Governance**. This selection means that the Cloud Provisioning and Governance application can find the script include.

    3.  Close the System Settings window.

    4.  Navigate to **System Definition** &gt; **Script Includes**.

    5.  Click **New**.

    6.  Fill in the form fields \(see table\):

<table id="table_vzw_1qw_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Provide a descriptive name without spaces.

</td></tr><tr><td>

Accessible from

</td><td>

Select **All application scopes**.

</td></tr><tr><td>

Script

</td><td>

Enter this script:

</td></tr><tr><td colspan="2">

```

var SetFields = Class.create();
SetFields.prototype = {
	initialize: function() {
	},
	setStackName: function(){
		return gs.getUserName();
	},
	type: 'HideFormAttributes'
};

```

</td></tr><tr><td colspan="2">

The function `setStackName()` returns the user name of the catalog item requester. You can call this function from a blueprint rule action.

</td></tr></tbody>
</table>        ![Set fields script include](../image/blueprint-setfields-scriptinclude.png)

    7.  Click **Submit**.

    8.  Click the gear icon \(![System settings gear icon](../image/icon-gear-system-settings.png)\) in the upper left again, and then change the **Application** back to **Global**.

2.  In the Cloud Admin portal, navigate to **Design** &gt; **Blueprints** and open the relevant blueprint.

3.  On the blueprint form, click the **Catalog** tab, and then click the tile that represents the **Provision** operation.

    ![Catalog item](../image/request-operation-catalog-item.png)

4.  Click the **Stack Name** variable set in the Variable Sets related list.

    Notice that Stack Name is a single line text field that takes text input.

5.  Create a rule to populate the stack name:

    1.  Scroll down to the bottom of the form and click **New** in the **Rules** related list.

    2.  Provide a name and description.

    3.  Click **Submit**.

6.  Configure the action as follows:

    1.  From the Rule form, scroll down and click **New** in the **Action** related list.

    2.  Configure the rule as follows:

<table id="table_tgy_xlw_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Provide a meaningful name and description, such as `Set Stack Name to User ID`.

</td></tr><tr><td>

Action Type

</td><td>

Select **SetValueByScript** to tell the system to call the script include that you specify in the **Value** field.

</td></tr><tr><td>

Target Variable

</td><td>

Select **StackName** to tell the system to set the value of the Stack Name field.

</td></tr><tr><td>

Value

</td><td>

Call the method in the script include that returns the user ID. The call must be in the following syntax:`$(Script:ScriptIncludeName.methodName[])`

 In this example, use `$(Script:SetFields.setStackName[])`

</td></tr></tbody>
</table>        ![A script action on StackName](../image/blueprint-action-pop-stackname.png)

    3.  Click **Submit**.


## Result

In the Cloud User Portal, the catalog order form for the Provision operation shows the user ID of the logged-in user. This example uses the user Able Tutor, which comes in the base system as demo data. The value in the **Stack Name** field is the same value as in the User ID field on the User \[sys\_user\] table. The profile icon for the same logged in user is also displayed in the upper right of the Cloud User Portal.

![The Logged In User](../image/logged-in-user.png)

**Parent Topic:**[Cloud catalog form configuration examples](../concept/example-blueprint-rules.md)

