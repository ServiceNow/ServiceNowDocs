---
title: Define condition attributes on enterprise models and assets
description: Define the conditions to be inspected on enterprise models and assets throughout their life cycle.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Asset conditions, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Define condition attributes on enterprise models and assets

Define the conditions to be inspected on enterprise models and assets throughout their life cycle.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

Once condition attributes are defined on an enterprise model, all the assets for that models inherit the condition attributes.

Before defining condition attributes, create a condition template from the Admin center view. You can also create condition templates while defining condition attributes from the enterprise asset or enterprise model page.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace**.

2.  Navigate to either of the two views.

    -   Enterprise asset estate: For adding condition attributes to an asset.
    -   Enterprise model management: For adding condition attributes to a model.
3.  Select either the **All enterprise** tab or the tab for a specific model or asset category, such as Construction.

4.  From the list of available enterprise models or assets, open the enterprise model or asset that you want to define the condition attributes on.

5.  Select **New** on the Condition attributes related list.

6.  On the form, fill in the fields.

<table id="table_ln5_w4y_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Attribute details

</td></tr><tr><td>

Name

</td><td>

Name of the condition attribute.

</td></tr><tr><td>

Model or Asset

 The Model field appears in the Enterprise model management view. The Asset field appears in the Enterprise asset estate view.

</td><td>

The model or asset the condition attribute is being added to.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the condition attribute.

</td></tr><tr><td>

Weight

</td><td>

Desired weight for each line. The total sum of weights for all lines of an asset should equal one.

</td></tr><tr><td>

Attribute typeThis field appears only in the Enterprise asset estate view.

</td><td>

Type of attribute.

</td></tr><tr><td>

Category

</td><td>

Type of condition.**Note:** The Enterprise Asset Management application includes many default condition categories such as Area, Concentration, Density, and Electrical.

</td></tr><tr><td>

Condition template

</td><td>

The template that the condition is associated with.

 You can select an existing template or select **Create condition template** to create a template.

</td></tr><tr><td>

Criticality

</td><td>

Criticality level that indicates how important the condition attribute is.

</td></tr><tr><td>

Service frequency

</td><td>

Frequency at which you must perform the condition.

</td></tr><tr><td>

Pass condition minimum

</td><td>

Enter a minimum numerical value for the condition to pass. The value can't be less than zero.

</td></tr><tr><td>

Pass condition maximum

</td><td>

Enter a maximum numerical value for the condition to pass. The value can't be more than 100.

 For example, if you enter the value 100 in this field and the value 0 in the **Pass condition minimum** field, then if the overall score is between this range of 0-100, the result indicates that the condition passed.

</td></tr><tr><td>

Order

</td><td>

Order in which the condition attribute applies to the enterprise model or the asset. If your enterprise model or asset contains more than one condition attribute, the attribute with the lowest numerical value applies to the model or the asset first.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the condition attribute is active. Select this check box.

</td></tr></tbody>
</table>7.  Select **Save**.

    The form closes and you’re automatically redirected to the new condition attribute record.


**Parent Topic:**[Asset conditions in Enterprise Asset Management](../concept/asset-conditions-eam.md)

**Related topics**  


[Create condition templates for condition attributes](create-condition-template-eam.md)

