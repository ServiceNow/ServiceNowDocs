---
title: Submit an emergency maintenance request
description: Submit an emergency maintenance request for a meeting room.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-09-07"
reading_time_minutes: 3
breadcrumb: [Request a workplace service, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Submit an emergency maintenance request

Submit an emergency maintenance request for a meeting room.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home** &gt; **Catalog** on the navigation menu bar.

    You can also access the Emergency Maintenance request form using the Employee Center portal. Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace Services** &gt; **Maintenance** &gt; **Submit an emergency maintenance request**.

2.  Select **Submit an emergency maintenance request** record form.

    ![Submit an emergency maintenance request form.](../image/wsd-submit-emergency-request-form-use.png)

3.  Fill in the field information.

    |Field|Description|
    |-----|-----------|
    |Building|Building for which the maintenance request is raised.|
    |Floor|Floor where the maintenance is to be carried out.|
    |Space|Workspace which needs maintenance.|
    |Describe the issue|Short description of the maintenance case.|

4.  Select **Submit**.

    A workplace case is created and it is assigned automatically to the Workplace Event Planners assignment group. It is then assigned manually to a user in the Workplace Event Planners assignment group. For more information, see [View emergency maintenance case details](view-emergency-maint-case.md).

    When the emergency maintenance request case is assigned to a Workplace Event Planners assignment group, the AI agentic workflow **Manage temporary space closures** is triggered. The team of AI agents block a workspace location for maintenance. AI agents create a record in the sn\_wsd\_core\_block\_location table for blocking a location. If there are any impacted reservations for a blocked location, AI agents move any existing reservations to a new location.For more information, see [Manage temporary space closures agentic workflow](../../now-assist-wsd/concept/maintenance-meeting-room-agent-ai.md).


**Parent Topic:**[Request a workplace service](../concept/request-workplace-services.md)

**Related topics**  


[Reconfigure an office space](Reconfig-office-space-1.md)

[Raise help request for a workplace inquiry](submit-gen-workplace-serv-req.md)

[Raise a move request for a space change](../../workplace-move-mgmt/task/request-desk-change.md)

[Request furniture for a space](request-furniture.md)

[Raise a space assistance request](../../workplace-space-management/task/raise-a-space-recommendation-request.md)

[Submit a maintenance request](submit-a-maintenance-request.md)

[Submit a catering request](submit-a-catering-request.md)

[Submit heating and cooling request](submit-heating-and-cooling-request.md)

[Submit a badge request](submit-a-badge-request.md)

[Submit a tech support request](submit-a-tech-support-request.md)

[Submit a cleaning request](submit-a-cleaning-request.md)

[Submit an equipment request](submit-a-equipment-request.md)

[Edit a workplace request](edit-workplace-request.md)

[Submit a change event request for a reservation](submit-change-event-reservation.md)

