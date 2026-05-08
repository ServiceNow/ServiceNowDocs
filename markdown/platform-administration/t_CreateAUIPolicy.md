---
title: Using UI policies
description: UI policies dynamically change the behavior of information on a form and control custom process flows for tasks.Create a UI policy to define custom process flows for tasks.Create a UI policy to implement controls in the Incident form when the state changes to Resolved.Any scripts you create for UI policies run on the client side.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Using UI policies

UI policies dynamically change the behavior of information on a form and control custom process flows for tasks.

For example, you can use UI policies to make the number field on a form read-only, make the short description field mandatory, and hide other fields. Basic UI policies do not require any scripting, however for more advanced actions, use the **Run scripts** option.

You can also use client scripts to perform all of these actions, but for faster load times use UI policies when possible.

## Create a UI policy

Create a UI policy to define custom process flows for tasks.

Adding a UI Policy

### Before you begin

Role required: ui\_policy\_admin

### About this task

A UI policy condition evaluates all fields even if they are not visible on the form. This function removes the requirement that a field must be on a form for it to be evaluated.

**Note:**

-   Policies carried over from versions prior to Fuji are evaluated differently. Fields that previously were not evaluated are evaluated.
-   UI policies are not supported on search screens.
-   UI Policies also apply to forms and lists displayed within Content Management System application.

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Policies**.

2.  Click **New**.

    The UI Policy \[Advanced view\] form opens

3.  To change the view, in **Related Links** click **Default view**.

4.  Complete the form, as appropriate.

    You may need to configure the form to see all the fields.

<table id="table_d3l_g2l_dcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table for the form to be modified.

</td></tr><tr><td>

Active

</td><td>

The active status of the UI policy. Only active UI policies are applied.

</td></tr><tr><td>

Short description

</td><td>

Short summary of the UI policy.

</td></tr><tr><td>

Order \[Advanced view\]

</td><td>

The processing sequence, from the lowest to highest number. If two policies conflict, the UI policy with the higher number executes.For inherited UI policies, the extended \(child\) table's UI policies are executed first. Then the base table UI policies are executed; both from lowest to highest specified value.

</td></tr><tr><td class="sub-head" colspan="2">

When to Apply

</td></tr><tr><td>

Conditions

</td><td>

The conditions which, if fulfilled, cause the UI policy to be applied. Conditions are built with the condition builder. To set conditions using a script, use a client script instead. Conditions are only rechecked if a user manually changes a field on a form. If the change is made by a UI action, context menu action, or through the list editor, it is not evaluated.

</td></tr><tr><td>

Global \[Advanced view\]

</td><td>

Option for specifying whether the UI policy applies to all form views. If this check box is cleared, the UI policy is view-specific. By default, the Global UI policy applies to all form views. However, a UI policy can be specific to a view. For example, you can define a UI policy for only the itil view of a form. Use the **View** field to accomplish this.

</td></tr><tr><td>

View \[Advanced view\]

</td><td>

Option for indicating which form view the UI policy applies to. This field is visible only if **Global** is not selected. If Global is not selected and the View field is left blank, the script applies the default view. For more information on form views, see View management.

</td></tr><tr><td>

Reverse if false \[Advanced view\]

</td><td>

Option for specifying that the UI policy action is undone when the conditions of its UI policy evaluate to false. In other words, when the conditions are true, the specified actions are taken and when they are false, the actions are undone.

</td></tr><tr><td>

On load \[Advanced view\]

</td><td>

Option for specifying that the UI policy behavior should be performed OnLoad as well as when the form changes.You can check or clear the **On load** check box in a UI policy to control whether it runs every time a form is loaded when the conditions are satisfied. In this example, an administrator does not want an incident to enter the **Awaiting user info** state unless the user provides an explanation to the customer. The administrator creates a UI policy with the following settings.

-   In the When to Apply section, adds the condition **\[State\] \[is\] \[Awaiting user info\]** and clears the **On load** check box. This condition means that the UI policy applies only when the state is changed to **Awaiting user info**.
-   In the **UI Policy Actions** related list, creates a record that makes the **Additional comments** field mandatory when the condition is met.


</td></tr><tr><td>

Inherit \[Advanced view\]

</td><td>

Option for specifying whether extended tables inherit this UI policy.When a child table has an inherited UI policy from its parent table, the UI policy on the child table always runs first. This event is true regardless of the **Order** of the UI policies.

 Consider the following example:

-   A child table has a UI policy with **Order** value **500** that shows the **Urgency** field when its conditions are met.
-   Its parent table has a UI policy with the same conditions that hides the **Urgency** field. The parent table UI policy has **Order** value **100**.
-   Although the parent table **Order** field has a lower value, the child UI policy runs first and then the parent UI policy runs. When the conditions are met, the **Urgency** field is hidden.


</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Run scripts \[Advanced view\]

</td><td>

Option for specifying whether advanced behavior can be scripted for both true and false conditions.

</td></tr><tr><td>

Execute if true \[Advanced view\]

</td><td>

A script that executes when the conditions of the UI policy are fulfilled. -   This field is available only if **Run scripts** is selected.
-   This feature is not available outside the scope or in global scope.


</td></tr><tr><td>

Execute if false \[Advanced view\]

</td><td>

A script that executes if the conditions of the UI policy are not fulfilled and the **Reverse if false** option is selected.-   This field is available only if **Run scripts** is selected.
-   This feature is not available outside the scope or in global scope.


</td></tr><tr><td class="sub-head" colspan="2">

Other fields

</td></tr><tr><td>

Run scripts in UI type

</td><td>

The UI type for this UI policy: Desktop, Mobile / Service Portal, or Both.

</td></tr><tr><td class="sub-head" colspan="2">

Related List: UI Policy Actions

</td></tr><tr><td>

Table

</td><td>

\[read-only\] Field the UI policy action applies to.

</td></tr><tr><td>

Field name

</td><td>

Field on the selected table to which the UI policy performs an action if true.**Note:** If the specified field is not found on the form, the UI policy performs the action on the variable with the same name.

</td></tr><tr><td>

Mandatory

</td><td>

Choice list for specifying how the UI policy affects the mandatory state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td>

Visible

</td><td>

Choice list for specifying how the UI policy affects the visible state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td>

Read only

</td><td>

Choice list for specifying how the UI policy affects the read-only state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td class="sub-head" colspan="2">

Related Links

</td></tr><tr><td>

Default view or Advanced view

</td><td>

Changes the form view to the default or advanced view. The fields change based on the view.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Example: creating a UI policy

Create a UI policy to implement controls in the Incident form when the state changes to **Resolved**.

### Before you begin

Role required: ui\_policy\_admin

### About this task

This example demonstrates how to implement the following controls.

-   Make a **Close Notes** field mandatory.
-   Hide the **Opened by** field.
-   Make the **Priority**, **Severity**, and **Urgency** fields read-only.
-   Run a client script that displays an alert message.

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Policies**.

2.  Click **New**.

3.  Supply the following information.

    |Name|Input|
    |----|-----|
    |Table|Incident|
    |Conditions|\[Incident state\] \[is\] \[Resolved\]|
    |Reverse if false|Select this check box. If the incident state is not **Resolved**, the UI policy is reversed.|
    |On load|Select this check box to perform the actions when the form is loaded or when the condition changes.|

4.  Right-click the form header and select **Save** from the context menu.

    The **UI Policy Actions** related list appears.

5.  In the related list, click **New**.

6.  Provide the following information.

    |Name|Input|
    |----|-----|
    |Field name|Close notes. This UI action makes the Close notes field mandatory.|
    |Mandatory|True|
    |Visible|Leave alone|
    |Read Only|Leave alone|

7.  Click **Submit**.

8.  Repeat the process to create UI policy actions to hide the **Opened by** field, and to make the **Priority**, **Severity**, and **Urgency** fields read-only.


## Client scripts for UI policies

Any scripts you create for UI policies run on the client side.

You can use different options in the UI Policy form to control when and how the UI policy is applied. These options include client scripts, OnLoad execution, and view-specific UI policies. Administrators can use the UI Policy form to create client scripts that run onChange when the UI policy conditions are met \(**Execute if true**\) or not met \(**Execute if false**\).To display these scripting fields in the UI Policy form, in the Script section, select the **Run scripts** check box.

For example, to display an alert to the user when the incident **State** field changes to **Resolved**, create the following script in the **Execute if true** field.

```
function onCondition(){
alert('You changed the "Incident state" to Resolved. Please enter your comments in the "Close notes" field.');
}
```

Service catalog UI policies control the behavior of catalog item forms. Service catalog UI policies can be applied to a catalog item or a variable set. For more information about using UI policies for service catalog items, see Service catalog UI policy

