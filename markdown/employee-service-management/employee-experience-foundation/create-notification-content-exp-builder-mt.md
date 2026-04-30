---
title: Create Microsoft Teams notification content with Content Experience Builder
description: Create or place notification content into a bundle or stage for a Microsoft Teams campaign using Content Experience Builder.Campaign form to create Microsoft Teams notification content using the Content Experience Builder.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create Microsoft Teams campaigns with the Content Experience Builder, Sending notifications to employees using Microsoft Teams, Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Create Microsoft Teams notification content with Content Experience Builder

Create or place notification content into a bundle or stage for a Microsoft Teams campaign using Content Experience Builder.

## Before you begin

Role required: sn\_ca.campaign\_manager or sn\_cd.content\_admin

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select **New**.

3.  On the Campaign form, fill in the fields.

    For a description of the field values, see [Campaign form in the Content Experience Builder](create-notification-content-exp-builder-mt.md#).

4.  Click **Save** to remain on the campaign page.

    Clicking **Submit** returns you to the campaigns list.


## What to do next

Click **Next** or the **Schedule of Content** tab to add stages and content to the campaign: [Create Microsoft Teams campaign stages using the Campaign Builder Experience](create-campaign-stage-content-exp-mt.md)

**Parent Topic:**[Create Microsoft Teams campaigns with the Content Experience Builder](../concept/create-campaign-content-exp-builder-mt.md)

## Campaign form in the Content Experience Builder

Campaign form to create Microsoft Teams notification content using the Content Experience Builder.

<table id="table_pwr_1ny_h5b"><thead><tr><th>

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

State of the campaign.

 -   Draft: The campaign is in the creation process. When content and bundles are attached to the campaign, the **Publish** button appears in the form header.
-   Published: Activates all content for an audience.
-   Editing: The campaign is being edited.

</td></tr><tr><td>

Audience

</td><td>

Names of the users from the list who you want to see the content.

</td></tr><tr><td>

Approvers

</td><td>

User responsible for approving the campaign.

</td></tr><tr><td>

Start time

</td><td>

Date and time the campaign should launch.

</td></tr><tr><td>

End time

</td><td>

Date and time the campaign should end.

</td></tr><tr><td>

Re-evaluate campaign

</td><td>

Option for reviewing audience for a campaign.

 If the box is cleared, the **Content Experiences: Update Campaign Audience** scheduled job runs one time, after which the targeted audience is never re-evaluated or changed.

 Option to display the **Re-evaluate frequency** field so you can define how often you want the **Content Experiences: Update Campaign Audience** scheduled job to run.

 When your campaign is re-evaluated, the users dependent on the current audience criteria are removed or added.

</td></tr><tr><td>

Re-evaluate frequency

</td><td>

Frequency, in days, that you want to re-evaluate the audience. Audiences are re-evaluated after the **Content Experiences: Update Campaign Audience** scheduled job runs based on the value you enter here.

 This field appears only if the **Re-evaluate campaign** check box is selected.

 This field value overrides the default \(7 days\) value set in the **Campaign Re-evaluation** field in the Content Experiences system property. For more information, see [Properties installed with Content Experiences](../../employee-center/reference/properties-installed-with-content-auto.md).

</td></tr><tr><td>

Description

</td><td>

Descriptive information about the campaign.

</td></tr></tbody>
</table>