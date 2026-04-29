---
title: Create a campaign
description: Create a campaign to push communications and important information to your employees.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating campaigns, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a campaign

Create a campaign to push communications and important information to your employees.

## Before you begin

Role required: sn\_ca.campaign\_manager or sn\_cd.content\_admin

## About this task

Campaigns are organized in a hierarchical structure.

First, you create a campaign defining a title, state, audience, start and end times, and other information. For example, you can create a campaign that promotes open enrollment for health benefits, targeting new hires, and runs through the open enrollment period.

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

State of the campaign. This field is automatically set to draft. After you associate content and stages with the campaign, the **Publish** button will appear.

</td></tr><tr><td>

Audience

</td><td>

Audience that will view the content of a campaign. Click the Unlock Audience icon to select the audience that you want the campaign to target. For more information, see [Create an audience](ec-audiences.md).

**Note:** After a campaign is in the Published state, you cannot add users. To add new users to a published campaign, click the **Edit Campaign** button. Or, go to the specific content of a campaign and use the **Refine audience** field. For more information, see [Create content for a campaign](ecpro-manage-content.md).

</td></tr><tr><td>

Approvers

</td><td>

Users responsible for approving content before the campaign is published. When you click the Lookup using list icon, only users with the Campaign Approver sn\_ca.campaign\_approver role appear.

To send notifications to approvers, select **Publish with Approval**.

The approvers receive an email notification that you require their approval. For more information, see [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Email templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** If you select **Yes** in the **sn\_ca.all\_must\_approve** property, all approvers must approve before the campaign publishes. If you select **No**, only one approver is required.

</td></tr><tr><td>

Start time \(yyy-MM-dd HH:mm:ss\)

</td><td>

The date and time that a campaign should launch.**Note:** To publish a campaign, you must define the start date and time.

</td></tr><tr><td>

End time \(yyy-MM-dd HH:mm:ss\)

</td><td>

The date and time that a campaign should end.

</td></tr><tr><td>

Re-evaluate campaign

</td><td>

Option for reviewing the audience for a campaign.

 If the box is unchecked, the **Content Experiences: Update Campaign Audience** scheduled job runs one time after which the targeted audience is never re-evaluated or changed.

 Check the box to display the **Re-evaluate frequency** field so you can define how often you want the **Content Experiences: Update Campaign Audience** scheduled job to run.

 When your campaign is re-evaluated, it removes or adds users depending on the current audience criteria.

</td></tr><tr><td>

Re-evaluate frequency

</td><td>

The frequency, in days, that you want to re-evaluate the audience. Audiences are re-evaluated after the **Content Experiences: Update Campaign Audience** scheduled job runs based on the value you enter here.This field appears only after you select the **Re-evaluate campaign** check box.

 This field allows you to override the default \(7 days\) value that is set in the **Campaign Re-evaluation** field in the Content Experiences system property. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md).

</td></tr><tr><td>

Description

</td><td>

Descriptive information about the campaign.

</td></tr><tr><td>

Tracking on

</td><td>

Option for capturing analytics for your campaign. For more information about campaign analytics, see [Content Analytics](../concept/ecpro-content-automation-analytics.md).

 This field appears only when a tracking profile is selected from the **Tracking profile** field.

</td></tr><tr><td>

Tracking profile

</td><td>

Tracking profile to use for Content Experiences analytics. Profiles determine what data to capture for campaign analytics.Click the Lookup using list icon and select the tracking profile that you want to use.

</td></tr></tbody>
</table>4.  Click **Save** to remain on the campaign page.


## What to do next

Select **Clone Campaign** to copy the campaign, bundles or stages, and content. Cloning saves you time when creating a new campaign if information from the original campaign can be used in a new campaign.

Select **Next** or the **Schedule of Content** tab to view the **Schedule of content** and access the **Content library**, stages, and content of the campaign.

Select the **Portal preview** tab to show the content you want to appear in your campaign. You can use filters to determine what you want to preview from the portal or single content. For more information, see [Preview your portal](ecpro-campaign-preview-use.md) and [Preview single content](ecpro-campaign-pre-piece.md).

After completing all parts of a campaign, click the **Publish** button.

**Note:** To start your campaign immediately, ensure the Used to manage whether we want to trigger the campaign publishing process immediately after publishing the campaign \(sn\_ca.publish.campaign.immediately\) sys property is set to **Yes**. This works for campaigns that have a start date and time in the past or the time of publish. Changing this sys property is recommended for campaigns that target less than 100,000 users.

The Trigger Campaign Published Workflow business rule executes and the scheduled jobs are bypassed. The Campaign Targets tab populates with the targeted audience and content is delivered. There are several states that appear after you publish your campaign with the Used to manage whether we want to trigger the campaign publishing process immediately after publishing the campaign \(sn\_ca.publish.campaign.immediately\) sys property is set to **Yes**. The states are:

-   Targeting Audience: The audience is in the process of being built/defined.
-   Add Non-Portal Campaign Content: Email, SMS, Push, and To-do content are being added and ready to be distributed.
-   Delivering Content: The audience and content has been defined and in the process of delivering the content.

The other scheduled jobs related to re-evaluate a campaign and frequency are not affected by this sys property. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md).

Publishing a campaign prior to the start date enables the scheduled jobs to add users to the campaign and create and schedule the content for the campaign.

Campaign Targets show a list of users assigned to a campaign after the **Content Experiences: Update Campaign Audience** scheduled job runs.

**Note:** The **Publish** button only appears when at least one bundle or stage with content is attached to the campaign, a title, and start time. Publishing activates all content for a selected audience and duration.

