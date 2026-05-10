---
title: Create a service catalog variable
description: Create service catalogs variables to gather information from users ordering a catalog item, for example, to ask users which options they want for the item.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a service catalog variable

Create service catalogs variables to gather information from users ordering a catalog item, for example, to ask users which options they want for the item.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  Select the catalog item that you want to create a variable for.

3.  In the **Variables** related list, click **New**.

4.  Select the variable type.

    Only the applicable fields for the variable type are then displayed.

5.  In the form, fill the fields.

<table id="table_k3f_2d4_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

Read-only field that indicates which applications can use this variable.

</td></tr><tr><td>

Map to field

</td><td>

Maps the variable to a specific field on the table for the record producer.This field appears if the variable belongs to a record producer.

</td></tr><tr><td>

Type

</td><td>

The variable type that you want to create. For more information, see [Types of service catalog variables](../reference/r_VariableTypes.md).

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item using the variable.

</td></tr><tr><td>

Order

</td><td>

Order that the variable is placed on the page for the catalog item. The variables are organized from top to bottom from least to greatest order value. For example, a variable with an order value of 1 is placed above other variables with higher-order values.

</td></tr><tr><td>

Active

</td><td>

Check box to make the variable available for use

</td></tr><tr><td>

Mandatory

</td><td>

Check box to make the variable mandatory as part of the ordering process.**Note:** This behavior is applicable only on page load, and can be changed via client APIs.

</td></tr><tr><td>

Read only

</td><td>

Option to make a variable read only or editable.

</td></tr><tr><td>

Hidden

</td><td>

Option to hide a variable.

</td></tr><tr><td>

Unique

</td><td>

Option to disallow duplicate values for this variable within a multi-row variable set.**Note:**

-   This field appears only for a variable created in a multi-row variable set.
-   This behavior is applicable only in ServiceNow AI Platform, Service Portal, and variable editor in Agent Workspace.


</td></tr><tr><td>

Disable initial slot fill

</td><td>

Check box to determine whether to activate usage of caller-provided key-value pairs that pre-fill catalog item forms.

</td></tr><tr><td>

Selection Required

</td><td>

Check box to require users to select the check box variable. For example, use this option to require users to select an **I agree** check box for an agreement form. If users try to submit the agreement form without selecting the check box, an alert message is displayed to tell users that they must select the check box.

</td></tr><tr><td>

Global

</td><td>

If selected, the variable is available for all catalog tasks within service catalog workflows or execution plans by default. If deselected, the variable must be associated with individual catalog tasks.

</td></tr><tr><td>

Field

</td><td>

Field that the variable maps to.This field appears if the variable belongs to a record producer.

</td></tr><tr><td>

Record producer table

</td><td>

Table that the record producer creates a record in.This field appears if the variable belongs to a record producer.

</td></tr><tr><td>

Hide on grid

</td><td>

Configure the visibility of a variable on the grid layout within a multi-row variable set \(MRVS\) for a catalog item. By default, the check box is not selected.

 If you select it, the variable doesn’t appear on the MRVS grid, but it still appears on the MRVS form.

</td></tr><tr><td class="sub-head" colspan="2">

Question

</td></tr><tr><td>

Question

</td><td>

Question to ask users ordering the catalog item.

</td></tr><tr><td>

Name

</td><td>

A name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the **Question** field for all variable types except break, container split, and container end.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when users point to the variable. Enter a brief note to describe the purpose of the 'Question'.

</td></tr><tr><td>

Example text

</td><td>

Hint that is displayed in the question field before a user enters a value.Applicable for the following variables:

-   IP Address
-   Email
-   URL
-   Single Line Text
-   Wide Single Line Text
-   Multi Line Text
-   Date
-   Date/Time


</td></tr><tr><td>

Rich Text

</td><td>

Formatted label to be displayed on a catalog item form.Applicable for the Rich Text Label variable.

</td></tr><tr><td class="sub-head" colspan="2">

Annotation

</td></tr><tr><td>

Show help

</td><td>

If selected, displays the [help text](t_DefineHelpInformation.md) and instructions for the variable.**Note:**

-   It is not available for break and check box variables.
-   Help text and instructions are not available for a variable set.


</td></tr><tr><td>

Always Expanded

</td><td>

If selected, the **Help text** and **Instructions** field value are expanded by default when the catalog item page loads. This check box appears only when the **Show help** check box is selected.

 **Note:**

-   This field is also applicable in Service Portal.
-   This field is not applicable in the variable editor in Workspace and Catalog Item UIB component.
-   If the **Expand help for all questions** check box is selected at the catalog item level, then the **Always Expanded** field setting at the variable level is overridden.
-   If the **Expand help for all questions** check box is deselected at the catalog item level, then the **Always Expanded** field setting at the variable level is applicable.


</td></tr><tr><td>

Help tag

</td><td>

If the **Always Expanded** check box is deselected, click the value specified in this field to display the **Help text** and **Instructions** field values.This field is not applicable in the variable editor in Workspace and Catalog Item UIB component.

</td></tr><tr><td>

Help text

</td><td>

Help information for a service catalog variable.This field is applicable in ServiceNow AI Platform, Service Portal, and variable editor in Workspace, and Catalog Item UIB component.

 However, in Workspace and Catalog Item UIB component, you can view either help text or instructions. If both instructions and help text are available, you can view only the instructions.

 This field is not applicable for Break, CheckBox, Container End, Container Split, Macro, and UI Page variables. In Workspace and Catalog Item UIB component, this field is additionally not applicable for a Masked variable.

</td></tr><tr><td>

Instructions

</td><td>

Information that requires rich text formatting or adding images to support help information. This field is applicable in ServiceNow AI Platform, Service Portal, and variable editor in Workspace, and Catalog Item UIB component.

 However, in Workspace and Catalog Item UIB component, you can view either help text or instructions. If both instructions and help text are available, you can view only the instructions.

 In Workspace and Catalog Item UIB component, this field is additionally not applicable for a Masked variable.

 **Note:** For HTML tables, use sizes that are within the width of the variable.

</td></tr><tr><td class="sub-head" colspan="2">

Type Specifications \(The fields in this section vary for each variable type\)

</td></tr><tr><td>

Variable Width

</td><td>

Width for the variable on the catalog item page, to specify what percentage of the screen size that it can span. For details, see [Configure a default width for service catalog variables](configure-variable-width.md).This field appears for all variable types except for break, container end, container start, container split, container layout, and label variables.

</td></tr><tr><td>

Enable also request for

</td><td>

Option to allow a catalog item request to be submitted for multiple users. After you select this option, the **Also request for** field is displayed along with Requested For variable in a catalog item. -   This functionality is only applicable in Service Portal.
-   This field is applicable only for the Requested For variable.
For information about delegated request experience, see [Delegated request experience](../concept/delegated-request-exp.md).

</td></tr><tr><td>

Roles to use also request for

</td><td>

Option to specify the roles that can submit a catalog item request for multiple users. -   This functionality is only applicable in Service Portal.
-   This field is applicable only for the Requested For variable.
-   This field appears only when the **Enable also request for** check box is selected.
 **Note:** If no role is specified, anyone who has access to the catalog item can submit the request.

For information about delegated request experience, see [Delegated request experience](../concept/delegated-request-exp.md).

</td></tr><tr><td>

Choice direction

</td><td>

The direction in which the choice list is arranged. -   **Across**: Arranges choices horizontally.
-   **Down**: Arranges choices vertically.
 This field appears for lookup multiple choice variables.

 **Note:** The selected direction is also applicable in Service Portal.

</td></tr><tr><td>

Choice field

</td><td>

Table field to populate options for the variable. If no choices are defined for a field, then the variable loads field-related distinct values from the table.This field appears for select box variables.

</td></tr><tr><td>

Choice table

</td><td>

Table with values to populate in the **Choice field**.This field appears for select box variables.

</td></tr><tr><td>

Do not select the first choice

</td><td>

Check box to leave all options for the variable cleared on the catalog item page. If this check box is selected, the first choice for the variable selected by default.

 This field appears for multiple choice and numeric scale variables.

</td></tr><tr><td>

Dynamic ref qual

</td><td>

Dynamic qualifier. Select a dynamic filter to run a query against the reference field.This field appears for reference variables when **Use reference qualifier** is set to **Dynamic**.

</td></tr><tr><td>

Include none

</td><td>

Check box to include the **None** option in a list of choices.This field appears for lookup multiple choice, lookup select box, multiple choice, and select box variables.

</td></tr><tr><td>

Layout

</td><td>

Layout for a container, whether one or two columns.This field appears for container start variables.

</td></tr><tr><td>

List table

</td><td>

Table with the values for the list collector. The table should have a display column specified. This field appears for list collector variables.

</td></tr><tr><td>

Lookup source

</td><td>

The lookup source. Select `Table` or `Choices`. By default, Table is selected.

</td></tr><tr><td>

Lookup from table

</td><td>

Table from which values are obtained for users to select. The values from this table are populated in the **Lookup value field**.This field appears for lookup multiple choice and lookup select box variables, and when a **Table** lookup source is selected.

</td></tr><tr><td>

Lookup value field

</td><td>

Field in the lookup table that populates options for the variable.This field appears for lookup multiple choice and lookup select box variables, and when a **Table** lookup source is selected.

</td></tr><tr><td>

Lookup label field\(s\)

</td><td>

Comma-separated list of fields in the lookup table whose values are used to display options.This field appears for lookup multiple choice and lookup select box variables, and when a **Table** lookup source is selected.

</td></tr><tr><td>

Lookup price field

</td><td>

Field in the lookup table whose value is used to modify the price of the item being ordered.This field appears for lookup multiple choice and lookup select box variables, and when a **Table** lookup source is selected.

</td></tr><tr><td>

Lookup recurring price field

</td><td>

Field in the lookup table whose value is used to modify the recurring price of the item being ordered.This field appears for lookup multiple choice and lookup select box variables, and when a **Table** lookup source is selected.

</td></tr><tr><td>

Choice table

</td><td>

Use this field to specify the table that contains the desired choice list. It is only active when the **Lookup source** is set to `Choices`. The system queries the central choice table \(sys\_choice\) for all choice lists associated with the table you select here.

</td></tr><tr><td>

Choice field

</td><td>

Use this field to select the specific field \(or "element"\) from the Choice table whose options you want to display. For instance, if your Choice table is Incident \[incident\], you could select the **Priority**, **State**, or **Category** field to display the choices defined for it.

</td></tr><tr><td>

Choices depend on

</td><td>

Select another variable from the same catalog item to make this variable's choices dependent on it. This creates a dynamic filtering effect. The choices shown in the current variable will be filtered in real-time based on the value the user selects in the variable specified here. For example, if this field is for "City", you might select a "Country" variable here, ensuring only relevant cities are shown based on the selected country.

</td></tr><tr><td>

Macro

</td><td>

[UI macro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_UIMacros.md) to insert into the catalog item.This field appears for macro, macro with label, and UI page variables.

</td></tr><tr><td>

Summary macro

</td><td>

Applicable only for Marco, and Macro with Label type variables.

</td></tr><tr><td>

Widget

</td><td>

Applicable only for Marco, and Macro with Label type variables.

</td></tr><tr><td>

Price if checked

</td><td>

Price of the item.This field appears for check box variables.

</td></tr><tr><td>

Recurring price if checked

</td><td>

Price that increments for the item, when the user requests more than one order of the item.This field appears for check box variables. For more information about prices and recurring prices, see [Using variables for price setup](../concept/c_ServiceCatalogVariablePricing.md#).

</td></tr><tr><td>

Reference

</td><td>

Reference table for the variable. The table should have a display column specified.This field appears for reference variables.

</td></tr><tr><td>

Reference qual

</td><td>

Qualifiers to restrict data that is available in the field.Supports reference qualifiers and advance qualifiers. For more information, see [Reference qualifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceQualifiers.md).

 Returns all matching results \(no maximum\).

 **Note:** For security reasons, the use of scripts in the **Reference qual** field is restricted to system administrators through the **Allow javascript in Default Value** business rule.

 This field appears for list collector, lookup multiple choice, lookup select box, reference and Requested For variables.

 It appears for reference variables when **Use reference qualifier** is set to **Dynamic**.

</td></tr><tr><td>

Reference qualifier condition

</td><td>

Options to build conditions.This field appears for reference variables when **Use reference qualifier** is set to **Simple**.

</td></tr><tr><td>

Scale max

</td><td>

Highest value on the scale of available options for the variable. This field appears for numeric scale variables.

</td></tr><tr><td>

Scale min

</td><td>

Lowest value on the scale of available options for the variable. This field appears for numeric scale variables.

</td></tr><tr><td>

Unique values only

</td><td>

Check box to require a unique value for the field. When this check box is selected, two records cannot have the same value for that field.This field appears for lookup multiple choice, lookup select box, and select box variables.

</td></tr><tr><td>

Use confirmation

</td><td>

Check box to prompt users to reenter data to verify their entries.This field appears for masked variables.

</td></tr><tr><td>

Use encryption

</td><td>

Check box to store the answer in encrypted format in the database. If not encrypted, the answer is stored in plain text format. Encryption uses Triple DES with system encryption.This field appears for masked variables.

</td></tr><tr><td>

Use reference qualifier

</td><td>

Type of qualifier to use.This field appears for reference variables.

</td></tr><tr><td>

Validation Regex

</td><td>

Regular expression that validates the variable value. This field is displayed only for Single Line Text and Wide Single Line Text variable types.To define regular expressions, see [Define a regular expression for a variable](define-regex-vrble.md).

 **Note:**

-   This field is also applicable in Service Portal.
-   The max\_length attribute value is valid even when the validation regex is set.
-   You cannot add a catalog item with regex validation errors to the wishlist.


</td></tr><tr><td>

Variable attributes

</td><td>

Attributes that define the behavior and restrictions for a variable. For information on variable attributes, see [Service catalog variable attribute](../reference/variable-attributes.md).

</td></tr><tr><td>

Topic block

</td><td>

Specify the topic block similar to configured UI macros or widgets used in the custom or custom with label variables to replicate the same behavior in a Virtual Agent conversation.

 **Note:** This field is available only for the "Custom" and "Custom with Label" variable types.

</td></tr><tr><td class="sub-head" colspan="2">

Default Value

</td></tr><tr><td>

Default value

</td><td>

Default value for the variable.

</td></tr><tr><td class="sub-head" colspan="2">

PermissionIf no role is specified in this tab for the read, write, or create actions, all users who can access the catalog item can perform these actions irrespective of their role. For example, if no role is specified for the **Write roles** field, all users who can access the catalog item can edit the variable value in the variable editor.

 A user with a role that does not match any of the following roles cannot set variable values even through scripting.

 These roles are not available for Label, Break, Container Split, Container End, Macro, Macro with Label, and UI Page variables.

</td></tr><tr><td>

Read roles

</td><td>

Roles that can view the variable before or after requesting the catalog item or record producer. Only a user with the roles specified in this field can view the variable.

</td></tr><tr><td>

Write roles

</td><td>

Roles that can edit the variable in the variable editor after requesting the catalog item or record producer. If a user does not have the roles specified in this field, the variable is read-only in the variable editor.

</td></tr><tr><td>

Create roles

</td><td>

Roles that can create values for the variable before requesting the catalog item or record producer. If a user does not have the specified role, the variable is read-only before requesting the catalog item or record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Availability

</td></tr><tr><td>

Visible Elsewhere

</td><td>

If selected, the variable is visible in the item form before ordering the item, in VEditor after ordering the item, and in the cart view of the item.

</td></tr><tr><td>

Visible on Bundles

</td><td>

If selected, the variable is visible when the item is added to a bundle.

</td></tr><tr><td>

Visible on Guides

</td><td>

If selected, the variable is visible when it is added to an order guide, or when it is added to a catalog item that is included in the order guide.**Note:** If an order guide has too many items and variables, consider clearing this check box on as many items as possible, to improve loading performance on order guides.

</td></tr><tr><td>

Visible on Summaries

</td><td>

If selected, the variable is visible on any variable summarizer of the catalog item. In Service Portal, the variable is visible in the RITM ticket page and the Approval page.

 In Now Mobile, the variable is visible in the RITM and the Approval records.

</td></tr><tr><td>

Remove from Conversational Interfaces

</td><td>

If the catalog item has a variable that's making the item non-conversational, for example, a variable about pricing, then select the check box so that the catalog item becomes conversational.**Note:** This option doesn't apply to the a multi-row variable set \(MRVS\).

</td></tr></tbody>
</table>6.  Click **Submit**.


-   **[Define help information for a service catalog variable](t_DefineHelpInformation.md)**  
Enter help information for a variable to help users determine what info they must provide for a service catalog variable.
-   **[Service Catalog variable attributes](../reference/variable-attributes.md)**  
There are a few Service Catalog variables support specific attributes to define the behavior and restrictions for variables.
-   **[Define a question choice for a variable](define-question-choice-var.md)**  
Define a question choice for a variable with service catalog.

**Parent Topic:**[Service catalog variables](../concept/c_ServiceCatalogVariables.md)

