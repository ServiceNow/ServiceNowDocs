---
title: Installing Microsoft Teams for all Virtual Agent users
description: Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Microsoft Teams. Batch pre-linking enables your Virtual Agent users to immediately chat with a virtual agent and receive notifications without going through the initial authentication linking process.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-05-27"
reading_time_minutes: 2
breadcrumb: [Configure Virtual Agent for Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Installing Microsoft Teams for all Virtual Agent users

Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Microsoft Teams. Batch pre-linking enables your Virtual Agent users to immediately chat with a virtual agent and receive notifications without going through the initial authentication linking process.

## Before you begin

**Note:** In order to send notifications to users, the app must be installed to all users. The recommended approach for installing the app to users is [Microsoft Teams App Setup Policy](https://learn.microsoft.com/en-us/microsoftteams/teams-app-setup-policies). When a user gets added to the policy, Microsoft will install the app to the user, and send us an `installationUpdate` event. When the event is received, the conversation with the user starts and contains the welcome message.

To install the app otherwise, use the following directions.

-   [Install Conversational Integration with Microsoft Teams](teams-install.md), with the **Automatically Link ServiceNow user profiles** option enabled.
-   [Set up Microsoft Teams Graph spoke](https://www.servicenow.com/docs/access?context=set-up-msteams&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
-   [Set up Microsoft Active Directory spoke](https://www.servicenow.com/docs/access?context=set-up-ad&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

Roles required:

-   virtual\_agent\_admin
-   external\_app\_install\_admin
-   One of the following Microsoft Teams administrator roles:
    -   Global Administrator
    -   Application Administrator
    -   Cloud Application Administrator
-   admin or schedule\_admin to change the scheduled job script

## About this task

When the **Automatically Link ServiceNow user profiles** option is enabled on the Settings page of the Manage Microsoft Teams channel, a batch of up to 10,000 users is automatically pre-linked to a ServiceNow instance. Your existing users are pre-linked during the initial run. Newly added users are pre-linked during subsequent daily runs.

To prevent automatic batch pre-linking, disable the **Automatically Link ServiceNow user profiles** option on the Messaging Apps Integration UI page.

Batch pre-linking of your Virtual Agent users to a ServiceNow instance before integrating with Microsoft Teams includes the following benefits:

-   Notifications are proactively sent by Virtual Agent to users when their identity in Microsoft Teams is associated with their identity in a ServiceNow instance. This is also true when the user is already linked with ServiceNow Virtual Agent.
-   If a user is pre-linked, and when Microsoft Teams notifications are enabled in the app, notifications are pushed to the app even when a user is not logged into a Microsoft Teams account.

Batch pre-linking happens automatically via the **MS Teams Daily Pre Install Job** scheduled job. This job runs by default daily at 1:00 a.m., but you can change the time, if desired. To modify the default scheduled job run time or time zone, access the **MS Teams Daily Pre Install Job** Scheduled Script Execution form.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for the **MS Teams Daily Pre Install Job** scheduled job and select to open the Scheduled Script Execution form for the selected record.

3.  In the **Run** field, change the run time to your desired time.

4.  For a description of the other fields that you can change in this form, including **Time zone**, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

5.  Select **Save**.


## What to do next

You can also customize the auto-linking process for Conversational Integration with Microsoft Teams. For more information, see [Customize auto-linking for Conversational Integration with Microsoft Teams](customize-autolink-msteams.md).

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

