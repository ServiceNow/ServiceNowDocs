---
title: Configure incidents to close automatically
description: Close incidents automatically based on the last updated date or the resolution date of the incident by configuring incident properties. You can also specify the number of days before resolved incidents close automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/configure-incident-auto-close.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident resolution and closure, Managing incidents, Incident Management, IT Service Management]
---

# Configure incidents to close automatically

Close incidents automatically based on the last updated date or the resolution date of the incident by configuring incident properties. You can also specify the number of days before resolved incidents close automatically.

## Before you begin

Role required: admin

## About this task

You can auto-close incidents based on the last updated date or the resolution date of the incident using the property **Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date** \(**com.snc.incident.autoclose.basedon.resolved\_at**\). This property is set to true only for new customers starting with the London release. Customers on releases earlier than London must set the property to true manually.

**Note:** You cannot auto-close a major incident based on the incident auto-closure property. For more information, see [Close a major incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/close-major-incident.md).

A scheduled job called **Autoclose Incidents** \(**System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**\) runs the **Incident Autoclose** business rule to close incidents as described. By default, it assigns the name of the administrator, who is logged in when the **Autoclose Incidents** job runs, to the **Updated by** field.

If the caller rejects the resolution of an incident, the state of the incident changes to **In Progress** and the incident isn't closed automatically.

## Procedure

1.  Navigate to **Incident** &gt; **Administration** &gt; **Incident Properties**.

2.  Select the **Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date** check box to auto-close incidents based on the resolution date.

3.  In the **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \(**glide.ui.autoclose.time**\) property, enter the number of days.

    **Note:**

    -   By default, the value is set to 7 business days.
    -   If you have an inactivity monitor triggering on your incident, it resets this auto-close clock each time it triggers, which stops the incident from closing. To avoid this reset, set a **Reset Condition** on your inactivity monitor to \[**Incident state**\] \[**is not**\] \[**Resolved**\].
4.  Select **Save**.


**Parent Topic:**[Incident resolution and closure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/c_IncidentResolutionAndRecovery.md)

**Related topics**  


[Configure the default user for auto-closing incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/change-default-user.md)

