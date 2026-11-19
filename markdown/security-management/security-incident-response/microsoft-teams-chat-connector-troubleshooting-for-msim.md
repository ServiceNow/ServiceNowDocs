---
title: Microsoft Teams Chat Connector troubleshooting for MSIM
description: Troubleshooting the scheduled jobs, system properties, and Microsoft Teams flow designer subflows for Microsoft Teams chat connector.Scheduled jobs are automated jobs that are run to process the notifications from Microsoft Teams chat connector and renew the Microsoft Teams subscriptions on a recurring schedule.View this section to understand the Microsoft Teams related flow designer subflows used to administer the Chat Channel\(s\) creation and user access from Major Security Incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/security-incident-response/microsoft-teams-chat-connector-troubleshooting-for-msim.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Teams, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Teams Chat Connector troubleshooting for MSIM

Troubleshooting the scheduled jobs, system properties, and Microsoft Teams flow designer subflows for Microsoft Teams chat connector.

Collaboration chat messages aren’t posted on:

-   Microsoft Teams.
-   The external collaboration activity stream of the MSIM workspace.

Verify the chat connector process scheduled jobs.

**Parent Topic:**[Configure Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/chat-channel-provider-config.md)

## Scheduled jobs for Microsoft Teams

Scheduled jobs are automated jobs that are run to process the notifications from Microsoft Teams chat connector and renew the Microsoft Teams subscriptions on a recurring schedule.

Collaboration chat messages aren’t posted on Microsoft Teams or the MSIM workspace.

Role required: admin.

Verify the following scheduled jobs:

-   **MS Teams Chat Connector: Process Notification**

    For each chat message event, a notification is received which has the Resource ID and the notification stored in a table. A schedule job is run for every 30 seconds to pick unprocessed notifications and query the Microsoft Teams API. This is performed to get the actual message contents, which are further stored in a different table.

-   **MS Teams Chat Connector: Renew Subscriptions**

    For each channel within the team, subscriptions are created to get notified of the created, updated, and deleted events. This subscription is active only for 60 minutes. The subscriptions are renewed every 25 minutes through the Microsoft Teams Connector: Renew Notification schedule job.


## Microsoft Teams Chat Connector Functional Flow

View this section to understand the Microsoft Teams related flow designer subflows used to administer the Chat Channel\(s\) creation and user access from Major Security Incident.

Chat channels aren’t created, or users can’t access them, from Major Security Incident.

Role required: sn\_msi.workspace\_admin

Navigate to **All** &gt; **Flow Designer** and verify the following subflows:

-   Add Members to Channel
-   Add Members to Team
-   Archive Team
-   Chat Team and Channels Creation
-   Create Channel Subscription
-   Create Channel with Users
-   Create Subscription for General Channel
-   Create Team
-   Delete Channel
-   Remove Members from Channel
-   Rename Channel
-   Renew Channel Subscription
-   Team and Channel Creation
-   Validate MS Teams Connection

