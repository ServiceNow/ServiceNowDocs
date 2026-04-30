---
title: Service Level Agreement \(SLA\) process example
description: As work is done on the relevant task, the SLA may change stage appropriately, depending on the information defined for that SLA in the relevant SLA definition.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Service Level Agreement \(SLA\) process example

As work is done on the relevant task, the SLA may change stage appropriately, depending on the information defined for that SLA in the relevant SLA definition.

## Before you begin

Role required: admin

## About this task

For example, if an incident is resolved within the time specified, the SLA stage is typically set to **Complete**.

Similarly, if the incident does not reach the required condition within the set amount of time, the Task SLA record associated to that Incident marked as **Has Breached**. For example, by default, if a P1 incident is not resolved within 8 hours, the Task SLA for that incident will have **Has Breached** set to **true**.

This example demonstrates how an SLA can be attached to an incident, then progressed to completion.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Create New**.

2.  Set both **Impact** and **Urgency** to **1**.

    This setting changes the **Priority** to **1 - Critical**.

3.  Save the form.

    The **Task SLA** Related List should now have a Priority 1 SLA attached to this incident.

    ![Task SLAs related list on Incident form - Priority 1 SLA](../image/TaskSLAIncidentForm-Priority1.png)

    **Note:** The default **Priority 1 resolution \(8 hour\)** SLA definition record is used to create and attach this Task SLA.

4.  Change the **Impact** to **2**, which changes the **Priority** to **2 - High**, then save the form.

    The Priority 1 SLA is now marked **Cancelled**, and a Priority 2 SLA has been attached, because of the conditions on the SLAs.

    ![Task SLAs related list on Incident form - Priority 2 SLA](../image/TaskSLAIncidentForm-Priority2.png)

5.  Change the **Incident State** to **Awaiting User Info**, then save the form.

    **Awaiting User Info** is a **Pause** condition on the Priority 2 SLA, so the SLA is marked **Paused**.

    **Note:** The pause duration on Task SLA gets updated only after the SLA moves out of pause.

    ![Task SLAs related list on Incident form - Priority 2 SLA paused](../image/TaskSLAIncidentForm-AwaitingUserInfo.png)

6.  Change the **Incident State** to **Active**, then save the form.

    Because the incident is no longer in a **Pause** condition, it resumes timing.

    ![Task SLAs related list on Incident form - Priority 2 SLA in progress](../image/TaskSLAIncidentForm-Active.png)

7.  Enter any **Close code** and **Close notes** values in the **Closure Information** section of the incident.

8.  Change the **Incident State** to **Resolved**, then save the form.

    The SLA is marked **Completed**.

    ![Task SLAs related list on Incident form - Priority 2 SLA completed](../image/TaskSLAIncidentForm-Resolved.png)


**Parent Topic:**[Service Level Management reference](../concept/service-level-management-reference.md)

