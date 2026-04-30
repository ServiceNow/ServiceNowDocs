---
title: Exploring Incident Management
description: ServiceNow Incident Management supports the incident management process with the ability to identify and log incidents, classify and prioritize incidents, assign incidents to appropriate users or groups, escalate, resolve, and report incidents.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Incident Management, IT Service Management]
---

# Exploring Incident Management

ServiceNow Incident Management supports the incident management process with the ability to identify and log incidents, classify and prioritize incidents, assign incidents to appropriate users or groups, escalate, resolve, and report incidents.

## Incident Management overview

Any user can record an incident and track it until service is restored and the issue is resolved. Each incident is generated as a task record that contains pertinent information. Incidents can be assigned to appropriate service desk members, who resolve the task and document the investigation. After the incident is resolved, you can manually close the incident. You can also close incidents automatically based on the last updated date or the resolution date of the incident. For more information about auto-closing incidents, see [Configure incidents to close automatically](../task/configure-incident-auto-close.md).

Any user can log an incident within the system using the following methods.

## Incident Management workflow

ServiceNow Incident Management process follows these steps:

1.  Incident identification - The first step in the life of an incident is incident identification. You can report incidents through emails, sms, phone call, support chats, walk-ups, and applications. The service desk decides if the issue is truly an incident or if it is a request.
2.  Incident logging - Once identified as an incident, the service desk logs the incident. The incident should include information, such as the caller, business service, configuration item, and contact type. The logging process includes:
    -   Incident categorization - Incident categorization is a vital step in the incident management process. Categorization involves assigning a category and at least one subcategory to the incident.
    -   Incident prioritization - Incident prioritization is important for SLA response adherence. The priority of an incident is determined by its impact on users or business and its urgency.
3.  Incident response - Once identified, categorized, prioritized, and logged, the service desk can handle and resolve the incident. Incident resolution involves the following steps:
    -   Initial diagnosis - Occurs when the user describes the problem and answers troubleshooting questions.
    -   Incident escalation - Happens when an incident requires advanced support, such as sending an on-site technician or assistance from certified support staff.
    -   Investigation and diagnosis - Takes place during troubleshooting when the initial incident hypothesis is confirmed as being correct. Once the incident is diagnosed, service desk can apply a solution, such as changing software settings, applying a software patch, or ordering new hardware.
    -   Resolution and recovery - Happens the service desk confirms that the service of the user is restored within the stipulated SLA time.
    -   Incident closure - At this point, the incident is considered closed and the incident process ends.

## Incident Management benefits

ServiceNow Incident Management supports the incident management process in the following ways:

-   Log incidents in the instance or by sending email.
-   Classify incidents by impact and urgency to prioritize work.
-   Assign to appropriate groups for quick resolution.
-   Escalate as necessary for further investigation.
-   Resolve the incident and notify the user who logged it.
-   Use reports to monitor, track, and analyze service levels and improvement.

Any user can record an incident and track it through the entire incident life cycle until service is restored and the issue is resolved.

-   **[Life cycle of an Incident](c_IncidentManagementStateModel.md)**  
Incident Management is responsible for managing the life cycle of incidents, from creation to closure.

**Parent Topic:**[Incident Management](c_IncidentManagement.md)

