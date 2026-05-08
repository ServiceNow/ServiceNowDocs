---
title: Create a notification destination in SRM
description: Set up notification destinations to help keep teams informed about service reliability.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Create a notification destination in SRM

Set up notification destinations to help keep teams informed about service reliability.

## Before you begin

Before creating notification destinations, set up the Microsoft Teams Graph spoke. When registering an application in the Microsoft Azure portal, grant the following Microsoft Teams Graph API permissions:

-   `ChannelMessage.Send`
-   `Group.ReadWrite.All**`

For setup instructions, see Set up the Microsoft Teams Graph spoke.

Role required: srm\_manager, srm\_admin, or admin

## About this task

Create a notification destination to deliver messages to a specific Microsoft Teams channel. After you set up a notification destination, team members can attach it to error budget policies to receive messages about policy breaches.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the primary navigation, select **Teams** \(![Teams icon](../../service-reliability/image/icon-sr-teams.png)\).

3.  On the Teams page, select the team you want to use the notification destination.

4.  Select the **SLO Notification destinations** tab, select **Create a destination**, and then fill out the form.

<table id="choicetable_q13_wwy_vfc"><thead><tr><th align="left" id="d87531e143">

Field

</th><th align="left" id="d87531e146">

Description

</th></tr></thead><tbody><tr><td id="d87531e152">

**Channel URL**

</td><td>

Deep link to the relevant Microsoft Teams channel. You can find deep links to channels in Microsoft Teams. They follow this general format: `https://teams.microsoft.com/l/channel/19%abcdef`.

</td></tr><tr><td id="d87531e172">

**Destination name**

</td><td>

Display name of the notification destination.Teams see this name when adding notification destinations to error budget policies.

</td></tr></tbody>
</table>5.  Select **Send test notification** to verify your setup.

    When successful, a message appears in the relevant Microsoft Teams channel. The message is titled `Test Notification` and includes the following text:

    ```
    This is a test notification from the Service Reliability Management (SRM) Team '<team-name>'.
    ```

6.  Select **Save**.

    The notification destination appears in the SLO Notification destinations tab. The table includes details about the Microsoft Teams channel and when the notification destination was last updated.


## What to do next

To use and learn more about notification destinations, visit the following pages:

-   [Create SLOs, SLIs, and error budget policies](sr-create-slo-sli.md)
-   [Notifications for breached error budgets](../reference/srm-notifications-messages.md)

You can also edit and delete notification destinations from the SLO Notification destinations tab. Deleting a notification destination removes it from all error budget policies where it was previously used.

**Parent Topic:**[Using SLO Management](using-service-level-objective-management.md)

