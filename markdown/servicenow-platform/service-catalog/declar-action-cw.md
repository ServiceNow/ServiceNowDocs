---
title: Create declarative actions for Service Catalog Wizards
description: Create and configure declarative actions to enable administrators to configure buttons \(wizard actions\) in Service Catalog Wizards.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Creating a Service Catalog Wizard, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create declarative actions for Service Catalog Wizards

Create and configure declarative actions to enable administrators to configure buttons \(wizard actions\) in Service Catalog Wizards.

## Before you begin

There are two types of declarative actions for catalog wizards:

-   UXF Client Action: Create declarative actions and map an action to a UIB page level event handler. Use this if you need to handle events at the UIB level such as opening a dialog box, or opening another catalog wizard, and so on.
-   Client Script: Use a client script that executes on a button click. Use this if you need to manipulate g\_form fields of the composite record producer that are linked to the catalog wizard.

The Catalog Wizard model is the declarative action model for catalog wizard which has the model fields that define the properties of the wizard. Use these fields to define what the payload can contain \(for UXF Client Action type\), or define conditions for button display on the wizard. Every wizard must use the Catalog Wizard model to create declarative actions.

Role required: wizard\_admin, admin

## Procedure

1.  Navigate to **Service Catalog Wizards &gt; Catalog Wizard Declarative Actions**.

    **Important:** Use this navigation path only to create declarative actions. This path sets the fields correctly when the declarative action form is loaded.

2.  Click **New** to create a new declarative action.

3.  Specify Catalog Wizard **Action Model Fields** to create payloads.

    The action model fields are available by default for catalog wizard declarative actions, and appear on the **Action Model Fields** tab in the **Action Assignment** form. ![Action Model fields](../image/catwiz-da-uxf.png)

    |Field|Description|
    |-----|-----------|
    |**Current Step Order**|Order of the current selected step.|
    |**Target Table**|Target table of the record producer or composite record producer used by the wizard.|
    |**Record Producer**|Sys\_id of the record producer or composite record producer used by the wizard.|
    |**Wizard Id**|Sys\_id of the wizard.|
    |**Enable Save**|Value of the **Enable Save** field on the wizard record.|
    |**Variables**|Object containing name and value for composite record producer variables associated with the wizard.|
    |**Is New Record**|The value is **True** when creating a new record using the wizard.|
    |**Template Id**|Sys\_id of the template applied on the wizard.|
    |**Has Review Step**|The value of the **Has Review Step** field on wizard record.|
    |**Is Last Step**|Indicates if it's the last step of the wizard. The last step is not dependent on order, and could change dynamically based on client scripting or UI policies of the wizard.|
    |**Form Dirty**|The value is **True** if the wizard has unsaved changes.|
    |**Submitting**|The value is **True** if a submission of the wizard is in progress.|
    |**Mode**|Mode in which the wizard is operating \(Template or Normal mode\).|
    |**Target Record Data**|Not Applicable \(this field is no used\).|
    |**Record Id**|Sys\_id of the record being created or edited by the wizard.|

4.  Click the **Action label** link for an action \(such as Insert or Delete\). ![Creating a declarative action](../image/catwiz-da-clientscript.png)

<table id="table_ics_3pj_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Action label**

</td><td>

Display label for the button on the wizard.

</td></tr><tr><td>

**Action name**

</td><td>

Identifier for the action.

</td></tr><tr><td>

**Implemented as**

</td><td>

UXF Client Action or Client Script for wizard declarative actions.

</td></tr><tr><td>

**Specify client action**

</td><td>

The payload definition if **Implemented as** is the UXF Client Action.

</td></tr><tr><td>

**Client Script**

</td><td>

If the **Implemented as** field value is Client Script, this value must be specified. **Important:** You can only use the variables on the CRP that are linked to the wizard.

</td></tr><tr><td>

**Tooltip**

</td><td>

Tooltip for the button.

</td></tr><tr><td>

**Button type**

</td><td>

Possible values are **Primary** or **Secondary**.

</td></tr><tr><td>

**Order**

</td><td>

Sequence that the button appears in.

</td></tr><tr><td>

**Group By**

</td><td>

Option that must be selected if the button is part of a group.

</td></tr><tr><td>

**Group**

</td><td>

The group the button belongs to, for the **Group By** option. Grouped buttons are displayed as a split button in the wizard.

</td></tr><tr><td>

**Scripted client conditions**

</td><td>

The conditions to be evaluated during button display. For example: `mode==‘template’&&variables.var==‘xxxx’`.**Note:** This field does not appear on the form by default.

</td></tr></tbody>
</table>5.  Click **Submit** to create the Wizard action.

6.  Navigate to **Service Catalog Wizards** &gt; **Catalog Wizard Actions Configurations** and click **New**.

    Create a Wizard Action Configuration record so you can use the declarative action in a wizard. Enter the following fields in the form.

<table id="table_v3g_34j_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Identifier of the wizard action configuration record.

</td></tr><tr><td>

**Declarative action**

</td><td>

Select a declarative action that was created using the Catalog Wizard model.

</td></tr><tr><td>

**Applies to**

</td><td>

The wizard mode in which this action should appear. The values are **Normal mode**, **Template mode**, or **All** \(both modes\).

</td></tr><tr><td>

**Global**

</td><td>

This action configuration applies to all wizards, regardless of whether it's mapped to a particular wizard or not. **Note:** The global actions **Save** and **Submit** are available by default.

</td></tr><tr><td>

**Overflow**

</td><td>

The button is displayed as part of overflow menu.

</td></tr><tr><td>

**Force Save**

</td><td>

Saves the wizard if any field values have been updated in the wizard before triggering the action.

</td></tr><tr><td>

**Label override**

</td><td>

Enter a label to override the label specified in the declarative action.

</td></tr><tr><td>

**Button type override**

</td><td>

The button type specified by the declarative action is overridden.

</td></tr></tbody>
</table>7.  Navigate to **Catalog Wizard** &gt; **Maintain Wizards**.

    To display a declarative action as a button on the wizard, map the Wizard Action Configuration with the Catalog Wizard.

    Open the wizard that you want to add the declarative action to. Use the related list **Wizard Actions Configurations** to create a mapping record between the wizard and the wizard action configuration.

    1.  Click **New** to create a new configuration directly.
    2.  Click **Edit** to attach an existing configuration to create a mapping record between the wizard and the configuration. The mapping record also has a toggle to hide a specific action.
    3.  Toggle the **Hide action** field to True to hide a specific action.

        **Tip:** Buttons with global configurations are available on the wizard by default. To hide a global action in a wizard, map the global configuration to the wizard and set the **Hide Action** to true.

    For more information on Catalog Wizards, see [Creating a Service Catalog Wizard](catalog-wizard.md).

8.  Use the **Configure declarative actions event mappings** action on the **Config** tab of UI Builder.

    Configure declarative actions event mappings is applicable only to UXF Client Action type of declarative action. Create a page level event handler, then map the declarative action to the page level event handler and specify the payload. For more information on binding events to declarative actions in UI Builder, see [Bind an event to a declarative action](https://www.servicenow.com/docs/access?context=bind-event-declarative-action&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


**Parent Topic:**[Creating a Service Catalog Wizard](catalog-wizard.md)

