---
title: Service Catalog variable form fields
description: Fields on the variable help you to define variables for a catalog item.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Service Catalog variable form fields

Fields on the variable help you to define variables for a catalog item.

<table id="table_yd3_v2c_3p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

Read-only field that indicates the application can use this variable.

</td></tr><tr><td>

Type

</td><td>

The variable type that you want to create.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item associated with the variable.

</td></tr><tr><td>

Order

</td><td>

Order in which the variable is placed on the catalog item page. The variables are organized with lowest order value on the top and greatest order value at the bottom.

</td></tr><tr><td>

Active

</td><td>

Option to make the variable available for use.

</td></tr><tr><td>

Mandatory

</td><td>

Option to mark the variable as required to order the catalog item.

</td></tr><tr><td>

Read only

</td><td>

Option to make the variable read only.

</td></tr><tr><td>

Hidden

</td><td>

Option to hide the variable.

</td></tr><tr><td class="sub-head" colspan="2">

Question tab

</td></tr><tr><td>

Question

</td><td>

Question to ask when ordering the catalog item.

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.**Note:**

If this field is empty, its value is auto-populated based on the **Question** field.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when you hover over the variable. Enter a brief note to describe the purpose of the Question.

</td></tr><tr><td>

Example text

</td><td>

Hint that is displayed in the question field before you enters a value. Applicable for the following variables:-   IP Address
-   Email
-   URL
-   Single Line Text
-   Wide Single Line Text
-   Multi Line Text
-   Date
-   Date/Time

</td></tr><tr><td class="sub-head" colspan="2">

Annotation

</td></tr><tr><td>

Show help

</td><td>

Option to provide additional help and instructions for the variable.

</td></tr><tr><td>

Help tag

</td><td>

Tag to display the Help text. For example, "More information."

</td></tr><tr><td>

Help text

</td><td>

Help information for a service catalog variable.

</td></tr><tr><td>

Instructions

</td><td>

Information that requires rich text formatting or adding images to support help information.

</td></tr><tr><td class="sub-head" colspan="2">

Type specificationsThe fields in this section vary for each variable type.

</td></tr><tr><td>

Variable Width

</td><td>

Width of the variable on the catalog item page, to specify what percentage of the screen size that it can span.

</td></tr><tr><td>

Enable also request for

</td><td>

Option to allow a catalog item request to be submitted for multiple users. After you select this option, the **Also request for** field is displayed along with **Requested For** variable in a catalog item.

</td></tr><tr><td>

Roles to use also request for

</td><td>

Option to specify the roles that can submit a catalog item request for multiple users.

</td></tr><tr><td>

Choice direction

</td><td>

The direction in which the list is arranged. -   **Across**: Arranges choices horizontally.
-   **Down**: Arranges choices vertically.

This field appears for lookup multiple choice variables.

</td></tr><tr><td>

Choice field

</td><td>

Table field to populate options for the variable. If no choices are defined for a field, then the variable loads field-related distinct values from the table.This field appears for select box variables.

</td></tr><tr><td>

Choice table

</td><td>

Table with values to populate in the **Choice field**.This field appears for select box variables.

</td></tr><tr><td>

Don’t select the first choice

</td><td>

Check box to leave all options for the variable cleared on the catalog item page.If this check box is selected, the first choice for the variable selected by default. This field appears for multiple choice and numeric scale variables.

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

Layout for a container.This field appears for container start variables.

</td></tr><tr><td>

List table

</td><td>

Table with the values for the list collector. The table should have a display column specified. For more This field appears for list collector variables.

</td></tr><tr><td>

Lookup from table

</td><td>

Table from which values are obtained for users to select. The values from this table are populated in the Lookup value field.This field appears for lookup multiple choice and lookup select box variables.

</td></tr><tr><td>

Lookup value field

</td><td>

Field in the lookup table that populates options for the variable.This field appears for lookup multiple choice and lookup select box variables.

</td></tr><tr><td>

Lookup label field\(s\)

</td><td>

Comma-separated list of fields in the lookup table whose values are used to display options.This field appears for lookup multiple choice and lookup select box variables.

</td></tr><tr><td>

Lookup price field

</td><td>

Field in the lookup table whose value is used to modify the price of the item being ordered.This field appears for lookup multiple choice and lookup select box variables.

</td></tr><tr><td>

Lookup recurring price field

</td><td>

Field in the lookup table whose value is used to modify the recurring price of the item being ordered.This field appears for lookup multiple choice and lookup select box variables.

</td></tr><tr><td>

Macro

</td><td>

UI macro to insert into the catalog item.This field appears for macro, macro with label, and UI page variables.

</td></tr><tr><td>

Summary macro

</td><td>

Applicable only for Macro, and Macro with Label type variables.

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

Price that increments for the item when you request more than one order of the item.This field appears for check box variables.

</td></tr><tr><td>

Reference

</td><td>

Reference table for the variable. The table should have a display column specified.This field appears for reference variables.

</td></tr><tr><td>

Reference qual

</td><td>

Qualifiers to restrict data that is available in the field. Supports reference qualifiers and advance qualifiers.This field appears for list collector, lookup multiple choice, lookup select box, reference, and Requested For variables. The field also appears for reference variables when **Use reference qualifier** is set to **Dynamic**.

</td></tr><tr><td>

Reference qualifier condition

</td><td>

Options to build conditions.This field appears for reference variables when **Use reference qualifier** is set to **Simple**.

</td></tr><tr><td>

Scale max

</td><td>

Highest value on the scale of available options for the variable.This field appears for numeric scale variables.

</td></tr><tr><td>

Scale min

</td><td>

Lowest value on the scale of available options for the variable.This field appears for numeric scale variables.

</td></tr><tr><td>

Unique values only

</td><td>

Check box to require a unique value for the field. When this check box is selected, two records can’t have the same value for that field.This field appears for lookup multiple choice, lookup select box, and select box variables.

</td></tr><tr><td>

Use confirmation

</td><td>

Check box to prompt users to reenter data to verify their entries.This field appears for masked variables.

</td></tr><tr><td>

Use encryption

</td><td>

Check box to store the answer in encrypted format in the database. If not encrypted, the answer is stored in plain text format.This field appears for masked variables.

</td></tr><tr><td>

Use reference qualifier

</td><td>

Type of qualifier to use.This field appears for reference variables.

</td></tr><tr><td>

Validation Regex

</td><td>

Regular expression that validates the variable value. This field is displayed only for Single Line Text and Wide Single Line Text variable types.

</td></tr><tr><td>

Variable attributes

</td><td>

Attributes that define the behavior and restrictions for a variable.

</td></tr><tr><td class="sub-head" colspan="2">

Default value

</td></tr><tr><td>

Default value

</td><td>

Default value for the variable.

</td></tr><tr><td class="sub-head" colspan="2">

Auto-populate

</td></tr><tr><td>

Dependent question

</td><td>

Reference type variable for the catalog item. This field is used to auto-populate the variable.

</td></tr><tr><td>

Reference

</td><td>

Reference field for auto-populating the variable.

</td></tr><tr><td class="sub-head" colspan="2">

PermissionIf no role is specified in this tab for the read, write, or create actions, all users who can access the catalog item can perform these actions irrespective of their role.

A user with a role that doesn’t match any of the following roles can't set variable values even through scripting.

These roles aren't available for Label, Break, Container Split, Container End, Macro, Macro with Label, and UI Page variables.

</td></tr><tr><td>

Read roles

</td><td>

Roles that can view the variable before or after requesting the catalog item or record producer. Only a user with the roles specified in this field can view the variable.

</td></tr><tr><td>

Write roles

</td><td>

Roles that can edit the variable in the variable editor after requesting the catalog item. If a user doesn’t have the roles specified in this field, the variable is read-only in the variable editor.

</td></tr><tr><td>

Create roles

</td><td>

Roles that can create values for the variable before requesting the catalog item or record producer. If a user doesn’t have the specified role, the variable is read only before requesting the catalog item or record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Availability

</td></tr><tr><td>

Visible Elsewhere

</td><td>

If selected, the variable appears on the item form before ordering the item, in the Variable Editor after ordering the item, and in the cart view of the item.

</td></tr><tr><td>

Visible on Bundles

</td><td>

If selected, the variable appears when the item is added to a bundle.

</td></tr><tr><td>

Visible on Guides

</td><td>

If selected, the variable appears when it’s added to an order guide, or when it’s added to a catalog item that is included in the order guide.**Note:** If an order guide has too many items and variables, consider clearing this check box on as many items as possible, to improve loading performance on order guides.

</td></tr><tr><td>

Visible on Summaries

</td><td>

If selected, the variable appears on any variable summarizer of the catalog item.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

