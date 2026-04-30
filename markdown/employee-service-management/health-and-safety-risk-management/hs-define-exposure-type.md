---
title: Define an exposure type
description: Identify and define a potential workplace exposure type present in a location in your organization. Maintain a list of all exposures types across your organization.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Safety exposure management, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define an exposure type

Identify and define a potential workplace exposure type present in a location in your organization. Maintain a list of all exposures types across your organization.

## Before you begin

Role required: sn\_hs\_rm.industrial\_hygienist or sn\_hs\_rm.exposure\_writer

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk management icon](../image/icon-risk-assessment.png)\).

3.  Select the **Exposure types** list and then **All**.

4.  Create an exposure or modify an existing one.

    -   To create an exposure, select **New**.
    -   To review an existing exposure, open the one that you want to modify.
5.  On the form, fill in the fields.

<table id="table_establishment"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the exposure type.

</td></tr><tr><td>

Location

</td><td>

Location where this exposure and the associated risks exists.

</td></tr><tr><td>

State

</td><td>

State of the exposure type.-   **Draft**: Select to configure the exposure type.​
-   **Active**: Select to mark this exposure type available for use. An exposure type must be active to be used.

The **Create exposure assessment** button for this exposure type appears when its state is set as active.

-   **Inactive**: Select to mark this exposure type as unavailable for use.
-   **Obsolete**: Select if this exposure type no longer exists.


</td></tr><tr><td>

Exposure category

</td><td>

Category for the exposure. The list in this field displays items from the choices defined for the `Exposure category` column in the Exposure type \[sn\_hs\_rm\_exposure\_type\] table.

</td></tr><tr><td>

Exposure sub-category

</td><td>

Subcategory for the exposure. This field appears only when a category is selected from **Exposure category** and subcategories are available for the selected category.

The subcategory choices for a category are defined in the `Exposure sub-category` column of the Exposure type \[sn\_hs\_rm\_exposure\_type\] table. For more information, see [Define a category for an exposure type](hs-define-category-measurement-unit-exposure-type.md).

</td></tr><tr><td>

Safety register

</td><td>

Safety register relevant to this exposure type. For example, if it's a chemical exposure, add a link it to corresponding safety register and the associated chemical safety data sheet.

</td></tr><tr><td>

Risk assessment

</td><td>

Risk assessment associated with this exposure type.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Add all exposure types that are present for a location.

8.  Select **Save**.

    The **Exposure assessments** tab appears for this exposure type.


## Result

The exposure type is listed in the **Exposure types** list and is saved in the Exposure type \[sn\_hs\_rm\_exposure\_type\] table.

## What to do next

1.  Create exposure assessment records for all locations in your organization that this exposure type applies to. For more information, see [Create an exposure assessment for an exposure type](hs-create-exposure-assessment.md).
2.  Perform exposure assessments across different locations for this exposure type. For more information, see [Perform an exposure assessment for a location](hs-perform-exposure-assessment.md).

**Parent Topic:**[Safety exposure management](../concept/hs-safety-exposures.md)

