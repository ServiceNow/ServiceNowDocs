---
title: Submit an emergency maintenance request
description: Submit an emergency maintenance request for a meeting room.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/submit-emergency-maint-request.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 3
breadcrumb: [Requesting a workplace service, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Submit an emergency maintenance request

Submit an emergency maintenance request for a meeting room.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home** &gt; **Catalog** on the navigation menu bar.

    You can also access the Emergency Maintenance request form using the Employee Center portal. Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace Services** &gt; **Maintenance** &gt; **Submit an emergency maintenance request**.

2.  Select **Submit an emergency maintenance request** record form.

3.  Fill in the field information.

    |Field|Description|
    |-----|-----------|
    |Building|Building for which the maintenance request is raised.|
    |Floor|Floor where the maintenance is to be carried out.|
    |Space|Workspace which needs maintenance.|
    |Describe the issue|Short description of the maintenance case.|

4.  Select **Submit**.

    A workplace case is created and it is assigned automatically to the Workplace Event Planners assignment group. It is then assigned manually to a user in the Workplace Event Planners assignment group. For more information, see [View emergency maintenance case details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/view-emergency-maint-case.md).

    When the emergency maintenance request case is assigned to a orkplace Event Planners assignment group, the AI agentic workflow **Manage temporary space closures** is triggered. The team of AI agents block a workspace location for maintenance. AI agents create a record in the sn\_wsd\_core\_block\_location table for blocking a location. If there are any impacted reservations for a blocked location, AI agents move any existing reservations to a new location.For more information, see [Manage temporary space closures agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/maintenance-meeting-room-agent-ai.md).


**Parent Topic:**[Requesting a workplace service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/request-workplace-services.md)

**Related topics**  


[Reconfigure an office space]()

[Raise help request for a workplace inquiry]()

[Raise a move request for a space change]()

[Request furniture for a space]()

[Raise a space assistance request]()

[Submit a maintenance request]()

[Submit a catering request]()

[Submit heating and cooling request]()

[Submit a badge request]()

[Submit a tech support request]()

[Submit a cleaning request]()

[Submit an equipment request]()

[Edit a workplace request]()

[Submit a change event request for a reservation]()

