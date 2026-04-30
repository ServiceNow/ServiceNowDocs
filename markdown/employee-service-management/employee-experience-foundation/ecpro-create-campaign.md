---
title: Create a campaign
description: Create a campaign to push communications and important information to your employees.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 3
breadcrumb: [Creating campaigns, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign

Create a campaign to push communications and important information to your employees.

## Before you begin

Role required: sn\_ca.campaign\_manager

If you would like to use Content Analytics to track the success of your campaign, you must set up a tracking profile and activate it. For more information, see [Content Analytics](../concept/ecpro-content-automation-analytics.md).

## About this task

Campaigns are organized in a hierarchical structure.

Create a campaign by defining a title, state, audience, start and end times, and other information. For example, you can create a campaign that promotes open enrollment for health benefits, targeting new hires, and runs through the open enrollment period.

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Click **New**.

3.  Fill in the following fields:

<table id="table_tkb_lzx_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Unique name for the campaign.

</td></tr><tr><td>

State

</td><td>

State of the campaign. This field automatically updates as you move through the campaign configuration process.

</td></tr><tr><td>

Audience

</td><td>

Audience that will view the content of a campaign. Click the Unlock Audience icon to select the audience that you want the campaign to target. For more information, see [Create an audience](ec-audiences.md).

</td></tr><tr><td>

Approvers

</td><td>

Users responsible for approving content before the campaign is published. When you click the Lookup using list icon, only users with the Campaign Approver sn\_ca.campaign\_approver role appear.

The approvers receive an email notification that you require their approval. For more information, see [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Description

</td><td>

Descriptive information about the campaign.

</td></tr><tr><td>

Start time \(yyy-MM-dd HH:mm:ss\)

</td><td>

The date and time that a campaign will launch.**Note:** To publish a campaign, you must define the start date and time.

</td></tr><tr><td>

End time \(yyy-MM-dd HH:mm:ss\)

</td><td>

The date and time that a campaign will end.

</td></tr><tr><td>

Re-evaluate campaign

</td><td>

Option for reviewing the audience for a campaign.

 Check the box to display the **Re-evaluate frequency** field to define how often you want the **Content Experiences: Update Campaign Audience** scheduled job to run.

 When your campaign is re-evaluated, it removes or adds users depending on the current audience criteria.

 If the **Re-evaluate campaign** box is unchecked, the **Content Experiences: Update Campaign Audience** scheduled job runs one time after which the targeted audience is never re-evaluated or changed.

</td></tr><tr><td>

Re-evaluate frequency

</td><td>

The frequency, in days, that you want to re-evaluate the audience. **Important:** To ensure that campaigns reflect any audience changes occurring since the last publication date, it is necessary to set the re-evaluation frequency.

Audiences are re-evaluated after the **Content Experiences: Update Campaign Audience** scheduled job runs based on the value you enter here.This field appears only after you select the **Re-evaluate campaign** check box.

 The value you set in this field overrides the default \(7 days\) value that is set in the **Campaign Re-evaluation** field in the Content Experiences system property. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md).

</td></tr><tr><td>

Tracking on

</td><td>

Enables Content Analytics to track metrics for this campaign.

</td></tr><tr><td>

Tracking profile

</td><td>

Tracking profile to use for Content Experiences analytics. Profiles determine what data to capture for campaign analytics.This field appears when the **Tracking on** option is selected.

Click the Lookup using list icon and select the tracking profile that you want to use.

</td></tr></tbody>
</table>4.  Click **Save** to remain on the campaign page.

    Clicking **Submit** returns you to the campaigns list.


## What to do next

Click **Next** or the **Schedule of Content** tab to add stages and content to the campaign: [Create campaign stages with Content Experience Builder](ecpro-campaign-builder.md)

