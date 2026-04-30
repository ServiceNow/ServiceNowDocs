---
title: Create adhoc incident communication plan from Incident Communications Management
description: Create an incident communication plan from Incident Communications Management when an issue is not considered earlier. If you need collaboration on that issue, you can create an incident communication plan.
locale: en-US
release: xanadu
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create adhoc incident communication plan, Manage, Incident Communications Management, IT Service Management]
---

# Create adhoc incident communication plan from Incident Communications Management

Create an incident communication plan from Incident Communications Management when an issue is not considered earlier. If you need collaboration on that issue, you can create an incident communication plan.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Create New**.

2.  On the form, fill in the fields.

    ![Incident communication plan form](../image/new-incident-communications-plan-form.png "Incident Communication Plan form")

    |Field|Description|
    |-----|-----------|
    |Number|Unique incident communication plan ID, in the ICPxxxxxxxx format.|
    |Source incident|The source incident for this communication plan, if any. If you select a source incident, the **Background** field is populated with data from this incident, unless there is existing data in this field.|
    |Type|Type of communication plan available are Ad hoc, End User, Stakeholder, and Technical.|
    |Communication plan definition|The communication plan definition based on which this incident communication plan is attached.|
    |State|The state of the communication plan. The available values are **Open**, **Closed**, or **Canceled**.|
    |Assignment group|The assignment group, if any, for that incident communication plan. For example, there might be a group that represents a crisis management team, including several Incident Managers, Duty Directors, and Duty Managers.|
    |Assigned to|The assigned user for the communication plan. By default, the assigned to user is the one who creates the communication plan. The communication plan can also be assigned to an ITIL user or an incident communication plan administrator.|
    |Order|Order in which the communication plan appears in the incident. If there are multiple communication plans, this field indicates which communication plan to execute first.|
    |Short description|A brief summary of the communication plan.|
    |Description|A detailed description of the communication plan.|
    |Notes|Work notes, activities, and background information regarding the incident communication plan.|

3.  Click **Submit**.

    An incident communication plan is created. The **Communication** tab lists the communication tasks that have email, SMS, or slack as the communication channel. The **Conference** tab lists the communication tasks that have conference as the communication channel.


**Parent Topic:**[Create adhoc incident communication plan](../concept/c_CreateIncidentAlerts.md)

