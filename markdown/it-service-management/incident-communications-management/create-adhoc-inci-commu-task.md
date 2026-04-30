---
title: Create adhoc incident communication task from Incident Communications Management
description: Create an adhoc incident communication task while you are working on the communication plan. The communication task helps you to specify the mode of communication \(channel\) and the frequency at which the communication must be carried out.
locale: en-US
release: yokohama
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Communications Management, IT Service Management]
---

# Create adhoc incident communication task from Incident Communications Management

Create an adhoc incident communication task while you are working on the communication plan. The communication task helps you to specify the mode of communication \(channel\) and the frequency at which the communication must be carried out.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

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

Create adhoc incident communication channel. For more information on how to define a communication channel, refer [Define a communication channel](https://www.servicenow.com/docs/access?context=create-comm-channel-definition&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

