---
title: Pre-link Virtual Agent requesters before integration with Slack
description: Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Slack. Batch pre-linking enables your Virtual Agent users immediately to chat with a virtual agent and receive notifications without going through the initial authentication linking process.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure VA settings for Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Pre-link Virtual Agent requesters before integration with Slack

Pre-link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Slack. Batch pre-linking enables your Virtual Agent users immediately to chat with a virtual agent and receive notifications without going through the initial authentication linking process.

## Before you begin

-   [Manage the ServiceNow Virtual Agent integration with Slack](configure-va-slack.md), with the **Automatically Link ServiceNow user profiles** option enabled.
-   [Set up Slack Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/set-up-slack.md).

Roles required:

-   virtual\_agent\_admin
-   external\_app\_install\_admin
-   One of the following Slack administrator roles:
    -   Global Administrator
    -   Application Administrator
    -   Cloud Application Administrator
-   admin or schedule\_admin to change the scheduled job script

## About this task

When the **Automatically Link ServiceNow user profiles** option is enabled on the Messaging Apps Integration UI page, a batch of up to 10,000 users is automatically pre-linked to a ServiceNow instance. Your existing users are pre-linked during the initial run. Newly added users are pre-linked during subsequent daily runs.

To prevent automatic batch pre-linking, disable the **Automatically Link ServiceNow user profiles** option on the Messaging Apps Integration UI page.

Batch pre-linking of your Virtual Agent users to a ServiceNow instance before integrating with Slack includes the following benefits:

-   Notifications are proactively sent by the Virtual Agent to users when their identity in Slack is associated with their identity in a ServiceNow instance. This is also true when the user is already linked with the ServiceNow Virtual Agent.
-   If a user is pre-linked, and when Slack notifications are enabled in the app, notifications are pushed to the app even when a user is not logged into a Slack account.

Batch pre-linking happens automatically via the **Slack Daily Pre-Link Job** scheduled job. This job runs by default at a scheduled time \(time is displayed in the time zone of the system administrator\) and you can change the time, if desired. To modify the default scheduled job run time or time zone, access the **Slack Daily Pre-Link Job** Scheduled Script Execution form.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for the **Slack Daily Pre-Link Job** scheduled job and click to open the Scheduled Script Execution form for the selected record.

3.  In the **Run** field, change the run time to your desired time.

4.  For a description of the other fields that you can change in this form, including **Time zone**, see [Automatically run a script of your choosing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_ScheduleAScriptExecution.md).

5.  Click **Save**.


**Parent Topic:**[Configure Virtual Agent settings for Slack](configure-va-slack-settings.md)

