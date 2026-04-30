---
title: Configure incidents to close automatically
description: Close incidents automatically based on the last updated date or the resolution date of the incident by configuring incident properties. You can also mention the number of days system must wait before initiating the auto-closing functionality.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Incident resolution and closure, Manage, Incident Management, IT Service Management]
---

# Configure incidents to close automatically

Close incidents automatically based on the last updated date or the resolution date of the incident by configuring incident properties. You can also mention the number of days system must wait before initiating the auto-closing functionality.

## Before you begin

Role required: admin

## About this task

You can auto-close incident based on the last updated date or the resolution date of the incident using the property **Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date** \(**com.snc.incident.autoclose.basedon.resolved\_at**\). This property is set to true only for the new customers starting the London release. Existing customers before the London release have to manually set the property to true.

**Note:** You cannot auto-close a major incident based on the incident auto-closure property. For more information, refer [Close a major incident](close-major-incident.md).

A scheduled job called **Autoclose Incidents** \(**System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**\) runs the **Incident Autoclose** business rule to close incidents as described. By default, it assigns the name of the administrator, who is logged in when the **Autoclose Incidents** job runs, to the **Updated by** field.

## Procedure

1.  Navigate to **Incident** &gt; **Administration** &gt; **Incident Properties**.

2.  Select the **Enable auto closure of incidents based on Resolution date. Setting this to 'No' will make auto closure to run based on the Updated date** check box if you want the incident to be auto-closed based on the resolution date.

3.  In the **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \(**glide.ui.autoclose.time**\) property, enter the number of days.

    **Note:** If you have an inactivity monitor triggering on your incident, it resets this auto-close clock each time it triggers, preventing your incident to be closed. To prevent this reset, set a **Reset Condition** on your inactivity monitor to **\[Incident state\] \[is not\] \[Resolved\]**.

4.  Click **Save**.


**Parent Topic:**[Incident resolution and closure](../concept/c_IncidentResolutionAndRecovery.md)

**Related topics**  


[Configure default user for auto-closing incidents](change-default-user.md)

