---
title: Create a campaign stage with condition trigger
description: This trigger is for Employee Journeys.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Campaign bundle triggers, Creating campaigns, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign stage with condition trigger

This trigger is for Employee Journeys.

## Before you begin

Role required: sn\_ca.campaign\_manager

Complete the steps to [Create a campaign](ecpro-create-campaign.md)

Create a stage with a to-do content item. For more information on this content type, see [To-do content](../concept/ec-to-do-content.md).

## About this task

Stages organize and manage the delivery of campaign content. When configuring a stage, you set the stage trigger, which determines when content becomes available and for how long.

**Note:** Some parts of the interface use the term "bundles" to refer to stages.

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select the campaign and click the **Schedule of content** tab or click **Next**.

    ![Schedule of content tab](../images/campaign-content-builder-1.png)

3.  Click **Create stage**.

    A stage is a visible area to add content.

    ![Campaign - Create stage](../images/campaign-create-stage.png)

4.  On the form, fill in the fields.

<table id="table_yb3_hrx_c3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition table

</td><td>

The table you want to use to create condition triggers for your campaign bundle.

</td></tr><tr><td>

User field

</td><td>

The fields from the table you selected that you want to create a condition that triggers your campaign bundle.

</td></tr><tr><td>

Start condition

</td><td>

Filter conditions based on the table and field you select for when you want the campaign bundle to trigger.

</td></tr><tr><td>

Offset trigger start

</td><td>

Indicates that you want the trigger to start after or before a defined number of days, weeks, or months from the trigger field you selected.

</td></tr><tr><td>

Date offset quantity

</td><td>

The number of date offset units \(days, weeks, or months\) the trigger date should occur.

</td></tr><tr><td>

Date offset units

</td><td>

The unit of time \(days, weeks, or months\) the date offset type should trigger.

</td></tr><tr><td>

When

</td><td>

Indicates if the trigger date should be before or after what you select in the trigger field.

</td></tr><tr><td>

**End** &gt; **Duration type**

</td><td>

Defines how long the content in this stage is available. Choose from:-   **Campaign end date** makes content available until the campaign ends.
-   **Time Length** ends content after a specific number of days or hours.
-   **Dynamic field** uses a trigger table and field to determine when content is no longer available. An example is to end content based on an employee's HR profile and start date.


</td></tr><tr><td>

**End** &gt; **Stop condition**

</td><td>

Filter conditions based on the table and field you select for when you want the campaign bundle to stop.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   Click **Add stage** to configure additional stages
-   Add content to the stage, specify an audience, and set the location where the content will be delivered. For more information on creating content in the Content Experience Builder, see [Add content to a campaign using Content Experience Builder](ecpro-campaigns-manage-content-builder.md)

