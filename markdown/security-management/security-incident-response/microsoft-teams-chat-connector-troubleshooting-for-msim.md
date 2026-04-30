---
title: MS Teams Chat Connector Troubleshooting for MSIM
description: Refer to Microsoft Teams chat connector troubleshooting section on the scheduled jobs, system properties, and Microsoft Teams flow designer subflows.Scheduled jobs are automated jobs that are run to process the notifications from Microsoft Teams chat connector and renew the Microsoft Teams subscriptions on a recurring schedule.View this section to understand the Microsoft Teams related flow designer subflows used to administer the Chat Channel\(s\) creation and user access from Major Security Incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Teams, Configuring Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# MS Teams Chat Connector Troubleshooting for MSIM

Refer to Microsoft Teams chat connector troubleshooting section on the scheduled jobs, system properties, and Microsoft Teams flow designer subflows.

Verify chat connector process scheduled jobs in any case if you don't see the collaboration chat messages are posted on Microsoft Team and on the external collaboration activity stream of the MSIM workspace.

**Parent Topic:**[Configure Microsoft Teams](chat-channel-provider-config.md)

## Scheduled Jobs for Microsoft Teams

Scheduled jobs are automated jobs that are run to process the notifications from Microsoft Teams chat connector and renew the Microsoft Teams subscriptions on a recurring schedule.

Role required: admin.

-   **MS Teams Chat Connector: Process Notification**

    For each chat message event, a notification will be received which will have the Resource ID and the notification which are stored in a table. A schedule job is run for every 30 seconds to pick unprocessed notifications and query Microsoft Teams API to get the actual message contents, which are further stored in a different table.

-   **MS Teams Chat Connector: Renew Subscriptions**

    For each channel within the team, subscriptions are created to get notified of the created, updated, and deleted events. This subscription is active only for 60 minutes. The subscriptions are renewed every 25 minutes through the Microsoft Teams Connector: Renew Notification schedule job.


## Microsoft Teams Chat Connector Functional Flow

View this section to understand the Microsoft Teams related flow designer subflows used to administer the Chat Channel\(s\) creation and user access from Major Security Incident.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Flow Designer**.

2.  Add Members to Channel

3.  Add Members to Team

4.  Archive Team

5.  Chat Team and Channels Creation

6.  Create Channel Subscription

7.  Create Channel with Users

8.  Create Subscription for General Channel

9.  Create Team

10. Delete Channel

11. Remove Members from Channel

12. Rename Channel

13. Renew Channel Subscription

14. Team and Channel Creation

15. Validate MS Teams Connection

    ![MS Teams flow designer sub flows](../image/msteams-flow-designer-subflows.png)


