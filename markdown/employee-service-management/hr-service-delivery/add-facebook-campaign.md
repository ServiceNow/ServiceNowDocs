---
title: Create a campaign for Workplace from Facebook
description: Create a campaign to publish content to the groups on Workplace from Facebook.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Employee Campaigns for Workplace from Facebook, Employee Campaigns for Workplace from Facebook, HR Service Delivery, Employee Service Management]
---

# Create a campaign for Workplace from Facebook

Create a campaign to publish content to the groups on Workplace from Facebook.

## Before you begin

Role required: sn\_ca.campaign\_admin, sn\_fb\_wp\_spoke.workplace\_fb\_admin

## Procedure

1.  Navigate to **Content Automation** &gt; **Campaigns**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_of4_jjt_wmb"><thead><tr><th>

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

-   Draft: The campaign is in the creation process. When content and bundles are attached to the campaign, the **Publish** button appears in the form header.
-   Published: Activates all content for an audience.
-   Editing: You have temporarily stopped the campaign to make edits.

**Note:** The campaign must be in the Published state to launch the content on Workplace from Facebook groups.

</td></tr><tr><td>

Audience

</td><td>

Audience that views the content of a campaign. **Note:** The values selected in this field are not applied for Workplace from Facebook content. For Workplace from Facebook content, the audience are Workplace from Facebook groups that are chosen from the Groups Cache \[sn\_fb\_wp\_spoke\_group\] table.

</td></tr><tr><td>

Approvers

</td><td>

Users responsible for approving the campaign.You require specific users to approve content before campaign publication.

 Only users with the Campaign Approver sn\_ca.campaign\_approver role appear after clicking the Lookup user list icon \(![Lookup user list icon](../image/magnifying-glass.png)\).

 After adding approvers, click **Update**.

 To send notifications to approvers, click **Publish with Approval**.

 Email notifies approvers that you require their approval. For more information, see Email Templates..

**Note:** If you select **Yes** in the **sn\_ca.all\_must\_approve** property, all approvers must approve before the campaign publishes. If you select **No**, only one approver is required.

</td></tr><tr><td>

Description

</td><td>

Descriptive information about the campaign.

</td></tr><tr><td>

Start time

</td><td>

Date and time that a campaign should launch.**Note:** To publish a campaign, you must define the start date and time.

</td></tr><tr><td>

End time

</td><td>

Date and time that a campaign should end.**Note:** This field is not applicable for Workplace from Facebook content. This implies that even if an end date and time is specified, the posts published to Workplace from Facebook groups as a part of Employee Campaigns are never removed.

</td></tr><tr><td>

Reevaluate campaign

</td><td>

Option for reviewing the audience for a campaign and overriding the default number of days to reevaluate your campaign.**Note:** This field is not applicable for Workplace from Facebook content. This implies that bundles containing Workplace from Facebook campaigns are never re-evaluated.

</td></tr><tr><td>

Reevaluate frequency

</td><td>

Frequency, in days, that you want to reevaluate the audience.**Note:** This field is not applicable for Workplace from Facebook content. This implies that after content is published to Workplace from Facebook groups as a part of Employee Campaigns, the groups are never reevaluated.

</td></tr></tbody>
</table>4.  Click **Submit**.


