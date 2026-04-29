---
title: Create a campaign stage with dynamic trigger
description: The campaign bundle triggers based on a trigger table \(sn\_hr\_core\_profile or sys\_user\), trigger field, and date offsets.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Campaign bundle triggers, Creating campaigns, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign stage with dynamic trigger

The campaign bundle triggers based on a trigger table \(sn\_hr\_core\_profile or sys\_user\), trigger field, and date offsets.

## Before you begin

Role required: sn\_ca.campaign\_manager

Complete the steps to [Create a campaign](ecpro-create-campaign.md)

## About this task

Stages organize and manage the delivery of campaign content. When configuring a stage, you set the stage trigger, which determines when content becomes available and for how long.

**Note:** Some parts of the interface use the term "bundles" to refer to stages.

![Dynamic trigger can be used for a welcome message in an onboarding campaign that lasts for 7 days after the employment start date](../images/dynamic-trigger.png)

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select the campaign and click the **Schedule of content** tab or click **Next**.

    ![Schedule of content tab](../images/campaign-content-builder-1.png)

3.  Click **Create stage**.

    A stage is a visible area to add content.

    ![Campaign - Create stage](../images/campaign-create-stage.png)

4.  On the form, fill in the fields.

<table id="table_shx_5vt_gxb"><thead><tr><th colspan="2">

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date table

</td><td>

 

</td><td>

The table you want to base your recurring campaign stage to trigger. Choose from:-   HR profile \(sn\_hr\_core\_profile\)
-   User \(sys\_user\)


</td></tr><tr><td>

Start date field

</td><td>

 

</td><td>

The fields from the table you select to base your recurring campaign stage to trigger. For example, if you are creating a recurring campaign stage for employee birthdays, select the HR profile table and **Date of birth** from this drop-down.

</td></tr><tr><td colspan="2">

Offset trigger start

</td><td>

Select this check box to trigger your campaign stage before or after the actual trigger start date. For example, if you are creating a recurring campaign stage for employee birthdays, you can trigger the campaign stage 2 days before the employee birthdays and keep the campaign stage active after the employee birthdays.**Note:** Content is not triggered unless the initial trigger is in the past. For example, if you set a yearly recurring trigger on a date in 2024, the content does not trigger until 2024, so the trigger must be set in the past. You can use the Offset trigger start field to pull the initial trigger start date before the current date.

</td></tr><tr><td>

 

</td><td>

Date offset quantity

</td><td>

The number of days, weeks, or months to offset the trigger type. This field works with the next fields to determine when content is available.For example, if you want your campaign stage to trigger 2 days before the actual date, enter 2 and select **Days** in the **Date** offset units drop-down.

</td></tr><tr><td>

 

</td><td>

Date offset units

</td><td>

Units of time to offset the trigger type.

</td></tr><tr><td>

 

</td><td>

When

</td><td>

Whether to offset the units before or after the set date.

</td></tr><tr><td>

**End****Duration type**

</td><td>

 

</td><td>

Defines how long the campaign stage is active. Choose from:-   **Campaign end date** makes content available until the campaign ends.
-   **Time Length** ends content after a specific number of days or hours.
-   **Dynamic field** uses a trigger table and field to determine when content is no longer available. An example is to end content based on an employee's HR profile and start date.


</td></tr><tr><td>

**Include audience members with trigger** &gt; **That occurs**

</td><td>

 

</td><td>

Specifies which audience members can view the content in the campaign stage, based on when their triggering event occurs. Choose from:-   **Anytime**: Includes all users in the campaign.
-   **During campaign**: Content is only available to users for whom the triggering event occurs after the campaign start date.
-   **After specified**: Content is available only to users for whom the triggering event occurs after a specific date.


</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   Click **Add stage** to configure additional stages
-   Add content to the stage, specify an audience, and set the location where the content will be delivered. For more information on creating content in the Content Experience Builder, see [Add content to a campaign using Content Experience Builder](ecpro-campaigns-manage-content-builder.md)

