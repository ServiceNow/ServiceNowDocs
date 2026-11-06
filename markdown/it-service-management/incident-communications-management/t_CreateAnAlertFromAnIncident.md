---
title: Create ad hoc incident communication plan from incident
description: Create an ad hoc incident communication plan from an incident to collaborate on an issue that isn't covered by an existing plan. Information from the incident automatically populates the ad hoc communication plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/t\_CreateAnAlertFromAnIncident.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Creating ad hoc incident communication plans, Managing incident communications, Incident Communications Management, IT Service Management]
---

# Create ad hoc incident communication plan from incident

Create an ad hoc incident communication plan from an incident to collaborate on an issue that isn't covered by an existing plan. Information from the incident automatically populates the ad hoc communication plan.

## Before you begin

Role required: major\_incident\_manager, ia\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open an existing incident.

3.  Select the Incident Communication Plans related list.

4.  Select **New**.

    The original incident becomes the source incident of this communication plan.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Automatically generated unique incident communication plan ID, in the ICPxxxxxxxx format.|
    |Source incident|Source incident for this communication plan, if any. If you select a source incident, the **Background** field is populated with data from this incident, unless there is existing data in this field.|
    |Type|Type of communication plan. The available values are Ad hoc, End User, Stakeholder, and Technical.|
    |Communication plan definition|Communication plan definition on which this incident communication plan is based.|
    |State|State of the communication plan. The available values are **Open**, **Closed**, and **Canceled**.|
    |Assignment group|Group, if any, assigned to the incident communication plan. For example, there might be a group that represents a crisis management team, including several Incident Managers, Duty Directors, and Duty Managers.|
    |Assigned to|User assigned to the communication plan. By default, the user who creates the communication plan is assigned. The communication plan can also be assigned to a user with the itil role or an incident communication plan administrator.|
    |Order|Order in which the communication plan appears in the incident. If there are multiple communication plans, this field indicates which communication plan to execute first.|
    |Short description|Brief summary of the communication plan.|
    |Description|Detailed description of the communication plan.|
    |Notes|Work notes, activities, and background information regarding the incident communication plan.|

6.  Select **Submit**.

    An incident communication plan is created. The **Communication** tab lists the communication tasks that have email, SMS, or Slack as the communication channel. The **Conference** tab lists the communication tasks that have conference as the communication channel.


**Parent Topic:**[Creating ad hoc incident communication plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/c_CreateIncidentAlerts.md)

