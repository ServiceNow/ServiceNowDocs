---
title: Create a campaign stage with to-do trigger
description: The content in a stage with a to-do trigger becomes available when a user completes a specific to-do item from another stage in the campaign. For example, create a stage that sends a confirmation email when an employee completes the "Select health plan" to-do item.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Campaign bundle triggers, Creating campaigns, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign stage with to-do trigger

The content in a stage with a to-do trigger becomes available when a user completes a specific to-do item from another stage in the campaign. For example, create a stage that sends a confirmation email when an employee completes the "Select health plan" to-do item.

## Before you begin

Role required: sn\_ca.campaign\_manager

Complete the steps to [Create a campaign](ecpro-create-campaign.md)

Create a stage with a to-do content item. For more information on this content type, see [To-do content](../concept/ec-to-do-content.md).

## About this task

Stages organize and manage the delivery of campaign content. When configuring a stage, you set the stage trigger, which determines when content becomes available and for how long.

**Note:** Some parts of the interface use the term "bundles" to refer to stages.

Create a stage that is triggered when the user completes a to-do item from another stage.

![Example to-do trigger setup](../images/todo-trigger.png)

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select the campaign and click the **Schedule of content** tab or click **Next**.

    ![Schedule of content tab](../images/campaign-content-builder-1.png)

3.  Click **Create stage**.

    A stage is a visible area to add content.

    ![Campaign - Create stage](../images/campaign-create-stage.png)

4.  On the form, fill in the fields.

<table id="campaign-bundle-fields"><thead><tr><th>

Field

</th><th>

 

</th><th>

Description

</th></tr></thead><tbody><tr id="row-title"><td colspan="2">

Title

</td><td>

The name of the campaign bundle.

</td></tr><tr id="row-campaign"><td colspan="2">

Campaign

</td><td>

The campaign associated with the campaign bundle.

</td></tr><tr><td colspan="2">

Trigger type

</td><td>

Select **To-do Completion**.

</td></tr><tr id="row-description"><td colspan="2">

Description

</td><td>

Descriptive information about the campaign bundle.

</td></tr><tr><td colspan="2">

Trigger item

</td><td>

The to-do item that activates the content in this bundle.

</td></tr><tr><td colspan="2">

Offset start date

</td><td>

Select this check box to trigger your campaign stage before or after the actual trigger start date.

</td></tr><tr><td colspan="2">

Date offset quantity

</td><td>

The number of days, weeks, or months to offset the trigger type.

</td></tr><tr><td colspan="2">

Date offset units

</td><td>

Units of time to offset the trigger type.

</td></tr><tr><td colspan="2">

When

</td><td>

Whether to offset the units before or after the set date.

</td></tr><tr><td colspan="2">

**End** &gt; **Duration type**

</td><td>

Defines how long the content in this stage is available. Choose from:-   **Campaign end date** makes content available until the campaign ends.
-   **Time Length** ends content after a specific number of days or hours.
-   **Dynamic field** uses a trigger table and field to determine when content is no longer available. An example is to end content based on an employee's HR profile and employment end date.


</td></tr><tr><td>

If you selected **Time Length**

</td><td>

Item duration

</td><td>

The number of days, hours, minutes, and seconds you want your campaign stage to remain active.

</td></tr><tr><td rowspan="6">

If you selected **Dynamic field**

</td><td>

End date table

</td><td>

Specify the table from which to select the condition that ends the campaign stage.

</td></tr><tr><td>

End date field

</td><td>

The fields from the table you selected that you want to create a condition that triggers your campaign bundle.

</td></tr><tr><td>

Offset end date

</td><td>

Select to indicate content availability ends after a specific amount of time.

</td></tr><tr><td>

Date offset quantity

</td><td>

The number of days, weeks, or months to offset the trigger type. This field works with the next fields to determine when content is available.

</td></tr><tr><td>

Date offset units

</td><td>

Units of time to offset from the content end date.

</td></tr><tr><td>

When

</td><td>

Whether to offset the units before or after the set date.

</td></tr><tr><td colspan="2">

Close other content

</td><td>

Select to make content from previous stages unavailable.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   Click **Add stage** to configure additional stages
-   Add content to the stage, specify an audience, and set the location where the content will be delivered. For more information on creating content in the Content Experience Builder, see [Add content to a campaign using Content Experience Builder](ecpro-campaigns-manage-content-builder.md)

