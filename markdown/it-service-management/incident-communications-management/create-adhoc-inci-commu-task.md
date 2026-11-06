---
title: Create an ad hoc incident communication task from Incident Communications Management
description: Create an ad hoc incident communication task while you're working on a communication plan. Use the task to specify the communication channel and how often the communication must be carried out.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/create-adhoc-inci-commu-task.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incident communications, Incident Communications Management, IT Service Management]
---

# Create an ad hoc incident communication task from Incident Communications Management

Create an ad hoc incident communication task while you're working on a communication plan. Use the task to specify the communication channel and how often the communication must be carried out.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open the incident communication plan for which you want to create the communication task.

3.  In the Incident Communication Tasks related list, select **New**.

4.  On the form, fill in the fields.

    | | |
    |---|---|
    |Number|Unique incident communication task ID, in the ICTxxxxxxxx format.|
    |Incident Communication Plan|Incident communication plan for which you create the task.|
    |Source incident|Incident to which the incident communication plan is attached.|
    |Type|Type of communication task, such as internal communication.|
    |Communication task definition|Unique name of the communication task definition for which you are creating the task.|
    |State|State of the communication task. The available values are **Pending**, **Open**, **In Progress**, **Complete**, and **Skipped**.|
    |Assignment group|Group, if any, assigned to the incident communication task.|
    |Assigned to|User assigned to the communication task.|
    |Order|Order in which the communication task appears in the communication plan. If there are multiple communication tasks, this field indicates which communication task to execute first.|
    |Communication frequency|Frequency of the communication task execution. You can send the notification once or repeatedly.|
    |Due in|Time by which the communication task must be completed.|
    |Last communication sent|Date and time of the most recent communication sent to the user or group.|
    |Short description|Brief summary of the communication task.|
    |Description|Detailed description of the communication task.|

5.  Select **Submit**.


## What to do next

Create an ad hoc incident communication channel. For instructions on defining a communication channel, see [Define a communication channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-comm-channel-definition.md).

**Parent Topic:**[Managing incident communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/working-with-inci-comm-mgmt.md)

