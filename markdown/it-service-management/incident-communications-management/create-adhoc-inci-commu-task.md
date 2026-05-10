---
title: Create adhoc incident communication task from Incident Communications Management
description: Create an adhoc incident communication task while you are working on the communication plan. The communication task helps you to specify the mode of communication \(channel\) and the frequency at which the communication must be carried out.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing Incident Communications, Incident Communications Management, IT Service Management]
---

# Create adhoc incident communication task from Incident Communications Management

Create an adhoc incident communication task while you are working on the communication plan. The communication task helps you to specify the mode of communication \(channel\) and the frequency at which the communication must be carried out.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident communication plan for which you want to create the communication task.

3.  In the Incident Communication Tasks related list and click **New**.

4.  On the form, fill in the fields.

    | | |
    |---|---|
    |Number|Unique incident communication task ID, in the ICTxxxxxxxx format.|
    |Incident Communication Plan|\[Read-only field\] Incident communication plan for which you create the task.|
    |Source incident|\[Read-only field\] Lookup icon ![Look up icon](../../itsm-workspace/image/look-up-icon.png) to select the incident on which you want the plan to be attached.|
    |Type|Lookup icon ![Look up icon](../../itsm-workspace/image/look-up-icon.png) to select the type of task such as internal communication.|
    |Communication task definition|\[Read-only field\] Unique name of the communication task definition for which you are creating the task.|
    |State|The state of the communication plan. The available values are **Pending**, **Open**, **In Progress**, **Complete**, and **Skipped**.|
    |Assignment group|The assignment group, if any, for that incident communication task.|
    |Assigned to|The assigned user for the communication task.|
    |Order|Order in which the communication task appears in the communication plan. If there are multiple communication tasks, this field indicates which communication task to execute first.|
    |Communication frequency|Frequency of the communication task execution. You can send the notification once or the notification can be repeated.|
    |Due in|Time by which the communication task must be completed.|
    |Last communication sent|The date and time when the last communication is sent to the user or the group.|
    |Short description|A brief summary of the communication task.|
    |Description|Detailed description of the communication task.|

5.  Click **Submit**.


## What to do next

Create adhoc incident communication channel. For more information on how to define a communication channel, refer [Define a communication channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/task-communications-management/create-comm-channel-definition.md).

**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

