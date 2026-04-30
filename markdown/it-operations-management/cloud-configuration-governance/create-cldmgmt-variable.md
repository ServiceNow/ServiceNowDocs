---
title: Edit a variable for Cloud Provisioning and Governance
description: Edit an existing cloud variable or create a new cloud variable to gather information for ordering a catalog item.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Edit a variable for Cloud Provisioning and Governance

Edit an existing cloud variable or create a new cloud variable to gather information for ordering a catalog item.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

You can edit a variable to change its type, for example from **Masked** to **Lookup Select Box**. You can also change the variable set of a variable, its order, make it active inactive, change its permission and availability options, and many more changes.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Open a catalog item, click the **Variable Sets** sub tab and click the variable set to which the variable to edit belongs to.

    All the cloud variables for the selected variable set appear under the **Cloud Variables** sub tab.

3.  Click the variable set that you want to edit.

4.  On the form, fill in the fields.

<table id="table_b3x_zzh_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Variable type to create. If you select **Lookup Select Box**, the **Type Specifications** subtab displays these fields:

-   **Use Pool Filter**: Select this check box to add a pool filter to the field.
-   **Pool**: Select a pool to offer the cloud service user a list of values from an existing table in the catalog order form. For example, you can select CloudAccountPool to get a list of all the cloud accounts.
-   **Pool Filter**: Select a filter to further narrow down the choices in the pool.


</td></tr><tr><td>

Variable Set

</td><td>

The variable set that the variable belongs to.

</td></tr><tr><td>

Mandatory

</td><td>

Option to make the variable mandatory as part of the ordering process.

</td></tr><tr><td>

Active

</td><td>

Option to make the variable available for use.

</td></tr><tr><td>

Order

</td><td>

Order that the variable is placed on the page for the catalog item. The variables are organized from top to bottom, from the least to greatest order value. For example, a variable with an order value of 1 is placed above other variables with higher-order values.

</td></tr></tbody>
</table><table id="table_x1h_t13_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Question to ask users ordering the catalog item.**Note:** If you select **Select Box** in the **Type** field, a **Question Choices** subtab appears at the end of the screen. You can enter a specific list of choices for the question.

</td></tr><tr><td>

Name

</td><td>

A name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the Question field for all variable types except break, container split, and container end, HTML, container start, label, UI page, and duration.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when users point to the variable. Enter a brief note to describe the purpose of the question.

</td></tr><tr><td>

Example text

</td><td>

Hint that's displayed in the question field before a user enters a value. Applicable for the following variables:-   IP address
-   Email
-   URL
-   Single Line text
-   Multi Line text
-   Date
-   Date/Time


</td></tr></tbody>
</table><table id="table_qzf_sb3_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Help

</td><td>

If selected, displays the help text for the variable.

</td></tr><tr><td>

Always Expanded

</td><td>

This option appears only when the **Show help** check box is selected.

If selected, the **Help text** field value is expanded by default when the catalog item page loads.

</td></tr><tr><td>

Help tag

</td><td>

If the **Always Expanded** check box is cleared, click the value specified in this field to display the **Help text** field value.

</td></tr><tr><td>

Help text

</td><td>

Help information for a service catalog variable.

</td></tr><tr><td>

Instructions

</td><td>

Information that requires rich text formatting or adding images to support help information.**Note:** For HTML tables, use sizes that are within the width of the variable.

</td></tr></tbody>
</table><table id="table_zn3_md3_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable Width

</td><td>

Width for the variable on the catalog item page, to specify what percentage of the screen size that it can span.This field appears for all variable types except for break, container end, container start, container split, container layout, and label variables.

</td></tr><tr><td>

Validation \(Regex\)

</td><td>

Regular expression that validates the user input for the property.

</td></tr><tr><td>

Validation Error \(Regex\)

</td><td>

If the expression isn't valid, an error appears.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Default Value|Default value for the variable.|
    |Variable Attributes|Attributes for this variable.|

    |Field|Description|
    |-----|-----------|
    |Read Roles|Roles that can view the variable before or after requesting the catalog item or record producer. Only a user with the roles specified in this field can view the variable.|
    |Write Roles|Roles that can edit the variable in the variable editor after requesting the catalog item or record producer. If a user doesn't have the roles specified in this field, the variable is read-only in the variable editor.|
    |Create Roles|Roles that can create values for the variable before requesting the catalog item or record producer. If a user doesn't have the specified role, the variable is read-only before requesting the catalog item or record producer.|

    | | |
    |---|---|
    |Visible|If selected, the variable is visible in the item form before ordering the item, in the Variable editor after ordering the item, and in the cart view of the item.|
    |Read-only|If selected, the variable is read-only in the Cloud User Portal and cannot be edited.|

5.  Click **Update** once you've made all the changes to the variable.


