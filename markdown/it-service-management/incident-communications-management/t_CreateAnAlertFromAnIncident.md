---
title: Create adhoc incident communication plan from incident
description: Create an adhoc incident communication plan from an incident when an issue related to the incident is not considered earlier. The incident automatically populates the required information in the adhoc communication plan, saving you time and effort.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create adhoc incident communication plan, Managing Incident Communications, Incident Communications Management, IT Service Management]
---

# Create adhoc incident communication plan from incident

Create an adhoc incident communication plan from an incident when an issue related to the incident is not considered earlier. The incident automatically populates the required information in the adhoc communication plan, saving you time and effort.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open an existing incident.

3.  Click the Incident Communication Plans related list.

4.  Click **New**.

    The original incident becomes the source incident of this communication plan.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Automatically generated unique incident communication plan ID, in the ICPxxxxxxxx format.|
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

6.  Click **Submit**.

    An incident communication plan is created. The **Communication** tab lists the communication tasks that have email, SMS, or slack as the communication channel. The **Conference** tab lists the communication tasks that have conference as the communication channel.


**Parent Topic:**[Create adhoc incident communication plan](../concept/c_CreateIncidentAlerts.md)

