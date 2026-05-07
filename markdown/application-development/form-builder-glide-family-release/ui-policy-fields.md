---
title: Policies and rules properties in Table Builder
description: You can configure the basic field policies and rules for any field that you work with in Table Builder.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Table Builder reference, Table Builder, Builder library, Developing your application, Building applications]
---

# Policies and rules properties in Table Builder

You can configure the basic field policies and rules for any field that you work with in Table Builder.

## UI Policies

The UI Policies section enables you to configure how forms appear based on roles and user input.

To understand the basic field properties, see [Create a UI policy in Table Builder](../concept/form-builder-policies-rules.md#).

The following table shows the field descriptions for the Policy details section when adding or editing a UI policy.

<table id="id_wdg_tvm_lsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Short summary of the UI policy.

</td></tr><tr><td>

Table

</td><td>

Data table that the policy applies to.

</td></tr><tr><td>

Domain

</td><td>

Domain that the choice resides in.

</td></tr><tr><td>

Order

</td><td>

Sequence for processing, from the lowest number to the highest number. If two policies conflict, the UI policy with the higher number runs.

 For inherited UI policies, the extended \(child\) table's UI policies run first. Then, the base table UI policies run, both from the lowest to the highest specified value.

</td></tr><tr><td>

Active

</td><td>

Status of the UI policy. Only active UI policies are applied.

</td></tr><tr><td>

Apply to all views/Apply to view \[Advanced settings\]

</td><td>

Option for specifying whether the UI policy applies to all form views or specific views. For more information on form views, see [View management](https://www.servicenow.com/docs/access?context=view-management-overview&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

On load \[Advanced settings\]

</td><td>

Option for specifying that the UI policy behavior should be performed OnLoad as well as when the form changes.

 Check or clear the UI policy **On load** check box to control whether it runs every time a form is loaded and conditions are satisfied. In the following example, an administrator does not want an incident to enter the **Awaiting user info** state unless the user provides an explanation to the customer. The administrator creates a UI policy with the following settings:

-   In the When these conditions are met section, adds the condition **\[State\] \[is\] \[Awaiting user info\]** and clears the **On load** check box. The UI policy applies only when the state is changed to **Awaiting user info**.
-   In the UI Policy Actions list, creates a record that makes the **Additional comments** field required when the condition is met.

</td></tr><tr><td>

Reverse if false \[Advanced settings\]

</td><td>

Option for specifying that the UI policy action should be reversed when the conditions of its UI policy evaluate to false. When the conditions are true, actions are taken and when they change back to false, the actions are reversed \(undone\).

</td></tr><tr><td>

Inherit \[Advanced settings\]

</td><td>

Option for specifying whether extended tables inherit this UI policy.

 When a child table has an inherited UI policy from its parent table, the UI policy on the child table always runs first, regardless of the **Order** of the UI policies. In the following example:

-   A child table has a UI policy with the**Order** value **500** that shows the **Urgency** field when its conditions are met.
-   Its parent table has a UI policy with the same conditions that hides the **Urgency** field. The parent table UI policy has the **Order** value **100**.
-   Although the parent table **Order** field has a lower value, the child UI policy runs first and then the parent UI policy runs. When the conditions are met, the **Urgency** field is hidden.

</td></tr></tbody>
</table>The following table shows field descriptions for the When these conditions are met section when adding or editing a UI policy.

<table id="id_u1v_svm_lsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition set

</td><td>

Conditions that, if fulfilled, cause the UI policy to be applied. Conditions are built with the condition builder by using logic statements. To set conditions using a script, use a client script instead.

 Conditions are only rechecked if a user manually changes a field on a form. If the change is made by a UI action, context menu action, or through the list editor, it is not evaluated.

</td></tr></tbody>
</table>The following table shows field descriptions for the Do the following section when adding or editing a UI policy.

<table id="id_rw2_svm_lsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Field on the selected table to which the UI policy performs an action if conditions are met.

**Note:** If the specified field is not on the form, the UI policy performs the action on the variable with the same name.

</td></tr><tr><td>

Mandatory

</td><td>

List for specifying how the UI policy affects the required state of the field. The choices are the following:

-   **Leave alone**
-   **True**
-   **False**

</td></tr><tr><td>

Visible

</td><td>

List for specifying how the UI policy affects the visible state of the field, that is, whether it appears. The choices are the following:

-   **Leave alone**
-   **True**
-   **False**

</td></tr><tr><td>

Read only

</td><td>

List for specifying how the UI policy affects the read-only state of the field. The choices are the following:

-   **Leave alone**
-   **True**
-   **False**

</td></tr><tr><td>

Clear the field value

</td><td>

Option to clear the specified field if the conditions are met.

</td></tr></tbody>
</table>## Access control rules

The Access control rules section enables you to configure access to the specified resource based on role, condition, and script criteria being met.

The following table shows field descriptions for the Access control rules section.

<table id="table_bpj_t1g_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Names each user who has permission to access the form or data. -   Enter the names as firstname.lastname in lower case letters, separated by a period \(for example, `john.smith`\). Each name must have a corresponding user record in **hi.servicenow.com**.
-   Enter multiple names and separate them by commas if multiple users have permission to access the form or data.
-   Enter an asterisk \(**\***\) as the name to enable all users to access the form or data.

</td></tr><tr><td>

Description

</td><td>

Overview of what the access control rule restricts or enables.

</td></tr><tr><td>

Type

</td><td>

Type of object the access controls, including the following:-   Client-callable script includes
-   Processor
-   Record
-   UI page
-   UX route

 For more information on object types, see [ACL matching requirements for objects](https://www.servicenow.com/docs/access?context=access-control-rules&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Operation

</td><td>

Type of action the system can take on the specified object, such as delete or execute. Some objects, such as records, support multiple operations, while other objects, such as a REST\_Endpoint, only support one operation. For more information on action types, see [ACL rule types](https://www.servicenow.com/docs/access?context=acl-rule-types&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Active state of the rule:-   **true**

The rule is active and available for use.

-   **false**

The rule is inactive and unavailable for use.


</td></tr><tr><td>

Condition

</td><td>

Any conditions that apply to the rule.

</td></tr><tr><td>

Roles

</td><td>

Any roles the rule applies to.

</td></tr><tr><td>

Admin overrides

</td><td>

Option to force the rule's evaluation for admin overrides at the access level. For more information on admin overrides, see [Evaluate the admin override at the access level](https://www.servicenow.com/docs/access?context=t_EvalAdmOverrideAccLevel&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Advanced

</td><td>

Option to associate a script with the rule.

</td></tr></tbody>
</table>## Client Scripts

The Client Scripts rules section enables you to create scripts that control how form fields appear based on defined criteria.

For a complete list of values for client script fields, see [Client script form](https://www.servicenow.com/docs/access?context=client-scripts&version=australia&pubname=australia-api-reference&ft:locale=en-US)

The following table shows field descriptions for the Client Scripts rules section.

<table id="table_e4d_1ph_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the script.

</td></tr><tr><td>

Description

</td><td>

Overview the script's functionality and purpose.

</td></tr><tr><td>

Table

</td><td>

Table or form that the script is available for.

</td></tr><tr><td>

Active

</td><td>

Active state of the script:-   **true**

The script is active and available for use.

-   **false**

The rule is inactive and unavailable for use.


</td></tr><tr><td>

UI type

</td><td>

Type of application the script is available for, such as desktop or mobile.

</td></tr><tr><td>

Type

</td><td>

When the script runs on the table or form, including the following:-   onCellEdit
-   onChange
-   onLoad
-   onSubmit

</td></tr><tr><td>

Field name

</td><td>

Field the script is run on.

</td></tr><tr><td>

View

</td><td>

Views on which the client script runs \(not applicable to global scripts\).

</td></tr><tr><td>

Inherited

</td><td>

Indicates whether the client script applies to extended tables.

</td></tr></tbody>
</table>## Business Rules

The Business Rules section enables you to create business rules to accomplish tasks like automatically changing values in form fields when certain conditions are met.

For a complete list of values for business rules, see [Create a business rule](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&section=t_CreatingABusinessRule&ft:locale=en-US).

The following table shows field descriptions for the Business Rules rules section.

<table id="table_a24_wtn_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the business rule.

</td></tr><tr><td>

Table

</td><td>

Table or form that the business rule runs on.

</td></tr><tr><td>

Active

</td><td>

Active state of the business rule:-   **true**

The business rule is active and available for use.

-   **false**

The business rule is inactive and unavailable for use.


</td></tr><tr><td>

When

</td><td>

When the business rule executes: **display**, **before**, **async**, or **after** the database operation is complete.

</td></tr><tr><td>

Filter conditions

</td><td>

Conditions created using the condition builder to determine when the business rule should run based on the field values in the selected table.

</td></tr><tr><td>

Role conditions

</td><td>

Roles that users who are modifying records in the table or form must have for the business rule to run.

</td></tr><tr><td>

Actions

</td><td>

Actions taken by the business rule on the specified fields, such as **insert**, **update**, and **delete**.

</td></tr><tr><td>

Set field values

</td><td>

Table or form fields that the action executes on.

</td></tr><tr><td>

Add message

</td><td>

Whether a message appears when this business rule is run:-   **true**

A message appears when the business rule is run.

-   **false**

No message appears when the business rule is run.


</td></tr><tr><td>

Abort action

</td><td>

Whether the business rule aborts the current database transaction:-   **true**

The business rule aborts the current database transaction when run.

-   **false**

The business rule doesn't abort the current database transaction when run.


 For example, on a before insert business rule, if the conditions are met, do not insert the record into the database.

</td></tr><tr><td>

Order

</td><td>

Indicates the sequence in which this business rule should run. If there are multiple rules on a particular activity, the rules run in the specified order specified, from lowest to highest.

</td></tr></tbody>
</table>## Workspace view rules

The Workspace view section enables you to define rules to control how users view workspaces based on criteria.

The following table shows field descriptions for the Workspace view rules section.

|Field|Description|
|-----|-----------|
|Name|Name for the workspace view rule.|
|Table|Table or form that the workspace view rule is available for.|
|View|View that is used to render the form. The default view is used if this field is left empty or contains an invalid value.|
|Roles|Any roles the rule applies to.|
|Conditions|Any conditions that apply to the rule.|
|Hide section navigation|Option to enable or disable section navigation.|
|Disable section collapsing|Option to enable or disable section collapsing.|
|Default tab order|Order in which form tabs appear by default.|

**Parent Topic:**[Table Builder reference](../concept/fb-reference.md)

