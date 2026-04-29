---
title: Create notification content for Microsoft Teams
description: Create notifications to send messages directly to your employees through Microsoft Teams.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a Microsoft Teams campaign using direct content publishing, Working on campaigns in Microsoft Teams, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create notification content for Microsoft Teams

Create notifications to send messages directly to your employees through Microsoft Teams.

## Before you begin

-   [Install the necessary plugins](../concept/using-campaigns-ms-teams.md)
-   Role required: sn\_cd.campaign\_manager
-   A Microsoft Teams notification includes a link [Create a video, URL, or to-do link](../../employee-center/task/ecpro-manage-link-content.md)

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Content Library**.

2.  Either use an existing content record or create a notification.

<table id="choicetable_chl_pby_h5b"><thead><tr><th align="left" id="d590126e97">

Record source

</th><th align="left" id="d590126e100">

Action

</th></tr></thead><tbody><tr><td id="d590126e106">

**Existing content record**

</td><td>

Select the content record from the list.

</td></tr><tr><td id="d590126e115">

**New content**

</td><td>

1.  Select **New**.
2.  Select **Notification** in the **Select the Platform** column.
3.  Select **Microsoft Teams**.
4.  Select **Continue**.


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

<table id="table_nyr_ws4_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the notification. The title is not the subject of the notification, although they can be identical.The default value is the app name provided in the manifest file. The value is appended with the phrase "posted a new campaign".

</td></tr><tr><td>

Subject

</td><td>

Subject of the notification, similar to the subject line in an email.

</td></tr><tr><td>

Description

</td><td>

Brief description of the notification.

</td></tr><tr><td>

Employee Center URL

</td><td>

The link to the video, web page, or to-do item that the notification directs the user to.

</td></tr><tr><td>

Content type

</td><td>

Option to select the type of notification that you want to send. This field is automatically set to Microsoft Teams.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the notification is active and available.

</td></tr></tbody>
</table>4.  Save the settings and return to the Content list.

    -   To save new content and settings, select **Submit**.
    -   To save existing content settings, select **Update**.

## What to do next

Make the content available to users: [Schedule delivery of Microsoft Teams notification content](schedule-delivery-content.md#).

Alternatively, you can build out a more robust publishing configuration using [Creating campaigns](../../employee-center/concept/ecpro-campaigns.md)

**Parent Topic:**[Create a Microsoft Teams campaign using direct content publishing](../concept/create-campaign-content-publishing.md)

