---
title: Create a campaign stage with recurring trigger
description: Use this trigger to publish date-based repeatable content. For example, recognition announcements like birthdays or work anniversaries.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Campaign bundle triggers, Creating campaigns, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign stage with recurring trigger

Use this trigger to publish date-based repeatable content. For example, recognition announcements like birthdays or work anniversaries.

## Before you begin

Role required: sn\_ca.campaign\_manager or sn\_cd.content\_admin

Complete the steps to [Create a campaign](ecpro-create-campaign.md)

## About this task

Stages organize and manage the delivery of campaign content. When configuring a stage, you set the stage trigger, which determines when content becomes available and for how long.

**Note:** Some parts of the interface use the term "bundles" to refer to stages.

![recurring trigger example](../images/recurring-trigger.png)

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select the campaign and click the **Schedule of content** tab or click **Next**.

    ![Schedule of content tab](../images/campaign-content-builder-1.png)

3.  Click **Create stage**.

    A stage is a visible area to add content.

    ![Campaign - Create stage](../images/campaign-create-stage.png)

4.  On the form, fill in the fields.

<table id="table_qv4_s5t_gxb"><thead><tr><th colspan="2">

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Frequency

</td><td>

Defines how often you want your announcement to repeat. Choose from:-   Daily
-   Weekly
-   Monthly
-   Yearly


</td></tr><tr><td colspan="2">

Start date table

</td><td>

The table you want to base your recurring campaign stage to trigger. Choose from:-   HR profile \(sn\_hr\_core\_profile\)
-   User \(sys\_user\)


</td></tr><tr><td colspan="2">

Start date field

</td><td>

The fields from the table you select to base your recurring campaign stage to trigger. For example, if you are creating a recurring campaign stage for employee birthdays, select the HR profile table and **Date of birth** from this drop-down.

</td></tr><tr><td colspan="2">

Offset start date

</td><td>

Select this check box to trigger your campaign stage before or after the actual trigger start date. For example, if you are creating a recurring campaign stage for employee birthdays, you can trigger the campaign stage 2 days before the employee birthdays and keep the campaign stage active after the employee birthdays.**Note:** Content is not triggered unless the initial trigger is in the past. For example, if you set a yearly recurring trigger on a date in 2024, the content does not trigger until 2024, so the trigger must be set in the past. You can use the Offset trigger start field to pull the initial trigger start date before the current date.

</td></tr><tr><td colspan="2">

Date offset quantity

</td><td>

The number of days, weeks, or months to offset the trigger type. This field works with the next fields to determine when content is available.For example, if you want your campaign stage to trigger 2 days before the actual date, enter 2 and select **Days** in the **Date** offset units drop-down.

</td></tr><tr><td colspan="2">

Date offset units

</td><td>

Units of time to offset the trigger type.

</td></tr><tr><td colspan="2">

When

</td><td>

Determines whether to trigger the stage content before or after the dates set in the campaign bundle.

</td></tr><tr><td colspan="2">

**End** &gt; **Item duration**

</td><td>

The number of days, hours, minutes, and seconds you want your campaign stage to remain active.

</td></tr><tr><td colspan="2">

**Include audience members with trigger** &gt; **That occurs**

</td><td>

Specifies whether the content in the stage becomes available to new audience members. Choose from:-   **Anytime**: Includes all users in the campaign.
-   **During campaign**: Content is only available to users for whom the triggering event occurs after the campaign start date.
-   **After specified**: Content is available only to users for whom the triggering event occurs after a specific date.


</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   Click **Add stage** to configure additional stages
-   Add content to the stage, specify an audience, and set the location where the content will be delivered. For more information on creating content in the Content Experience Builder, see [Add content to a campaign using Content Experience Builder](ecpro-campaigns-manage-content-builder.md)

