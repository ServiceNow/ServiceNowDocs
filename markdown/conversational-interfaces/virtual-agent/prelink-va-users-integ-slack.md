---
title: Link Virtual Agent requesters before integration with Slack
description: Link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Slack. Batch linking lets your Virtual Agent users chat immediately and receive notifications without going through the initial authentication linking process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/prelink-va-users-integ-slack.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Virtual Agent settings for Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Link Virtual Agent requesters before integration with Slack

Link your Virtual Agent requesters to a ServiceNow instance before they run the Conversational Integration with Slack. Batch linking lets your Virtual Agent users chat immediately and receive notifications without going through the initial authentication linking process.

## Before you begin

-   [Manage the ServiceNow Virtual Agent integration with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-va-slack.md), with the **Automatically Link ServiceNow user profiles** option enabled.
-   [Set up Slack Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/set-up-slack.md).

Roles required:

-   virtual\_agent\_admin
-   One of the following Slack administrator roles:
    -   Global Administrator
    -   Application Administrator
    -   Cloud Application Administrator
-   admin or schedule\_admin to change the scheduled job script

## About this task

When you enable the **Automatically Link ServiceNow user profiles** option, a batch of up to 10,000 users is linked automatically to a ServiceNow instance. Your existing users are linked during the initial run. Newly added users are linked during subsequent daily runs.

To prevent automatic batch linking, disable the **Automatically Link ServiceNow user profiles** option on the Messaging Apps Integration UI page.

Batch linking includes the following benefits:

-   Notifications are proactively sent by Virtual Agent to users when their identity in Slack is associated with their identity in a ServiceNow instance. This is also true when the user is already linked with Virtual Agent.
-   If a user is linked and Slack notifications are enabled in the app, notifications are pushed even when a user is not logged into a Slack account.

Batch linking happens automatically during the **Slack Daily Pre-Link Job** scheduled job. This job runs by default at a scheduled time \(time is displayed in the time zone of the system administrator\), and you can change the time, if desired. To modify the default scheduled job run time or time zone, access the **Slack Daily Pre-Link Job** Scheduled Script Execution form.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for the **Slack Daily Pre-Link Job** scheduled job and select it to open the Scheduled Script Execution form for the record.

3.  In the **Run** field, change the run time to your desired time.

4.  For a description of the other fields that you can change in this form, including **Time zone**, see [Automatically run a script of your choosing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_ScheduleAScriptExecution.md).

5.  Select **Save**.


**Parent Topic:**[Configure Virtual Agent settings for Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-va-slack-settings.md)

