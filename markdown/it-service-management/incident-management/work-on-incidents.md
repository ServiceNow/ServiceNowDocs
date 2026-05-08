---
title: Managing incidents
description: Working on incidents involves diagnosing and investigating the incident, recording results, and sometimes escalating or promoting the incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Incident Management, IT Service Management]
---

# Managing incidents

Working on incidents involves diagnosing and investigating the incident, recording results, and sometimes escalating or promoting the incident.

Initial diagnosis of incidents is largely a human process. The service desk agent looks at the details of the incident and communicates with the user to diagnose the issue.

To aid in the diagnosis, the service desk agent can query the configuration management database, or CMDB. The CMDB contains information about hardware and software within a network and the relationships between them. The CMDB can be populated by: Discovery . Discovery is available as a separate product.

## Incident investigation

Incident investigation is also a human process. The service desk continues to use the information in the Incident form as well as the CMDB to solve the issue. Work notes are added to the incident as the service desk evaluates the incident, facilitating communication between the concerned parties. Work notes and other updates can be communicated to the concerned parties through email notifications.

One way to investigate incidents is to determine whether related records exist, using one of the following features.

-   **Related incidents icon**

    The show related incidents icon \(![Show related incidents icon](../image/ShowRelatedIncidentsIcon.png)\) appears beside the **Caller** field when it is populated. Click the icon to view the list of incidents for the same caller.

    **Note:** Administrators can add this icon to any reference field by modifying the dictionary entry and adding the **ref\_contributions=user\_show\_incidents** dictionary attribute. The icon appears only for users who have read or write access to the field. A UI macro named user\_show\_incidents defines the behavior. The UI macro must be active to view the related incidents icon.

-   **Incidents by Same Caller related list**

    Another way to research related incidents is to use the **Incidents by Same Caller** related list. The administrator may need to configure the form to display this related list.

-   **Dependency views**

    Dependency views can help find related incidents based on configuration items \(CI\). If a configuration item is attached to an incident, click the map icon \(![Dependency view icon](../image/BusinessServiceMapIcon.png)\) to display the dependency views map. In the dependency map, if you want to view the tasks that are attached to the CI, click the down arrow next to the CI and from the menu, select **View Related Tasks**.

    ![CI options menu](../image/IM_CIOptionsDepViews.png "CI options")


## Incident promotion

When the incident management team has determined that the cause of an incident is an error or widespread problem, the team initiates the problem management process. When the issue requires a change to the infrastructure or a business service, the team initiates the change management process.

A menu item on the Incident form lets you create a problem or change record easily and associate the incident with the problem or change record. For more information, refer [Create a record from incident](../task/t_PromoteAnIncident.md)

**Note:** If the incident already has an associated problem or change record, you cannot create another record of the same task type.

Sometimes, the resolution for the user is to request hardware or software for them. For example, a user may report a problem that requires a new mouse device or keyboard. The service desk agent can create a request from the incident. The incident is associated with the requested item.

**Note:** This feature is available only in new instances starting with Jakarta or a later release. The Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\) plugin must be activated.

## Incident escalation

There are two escalation methods the platform uses to track and report on incidents that are not being resolved according to your organization standards.

-   **[Service level agreements](../../service-level-management/concept/service-level-management-concepts.md) \(SLAs\)**

    SLAs monitor the progress of an incident according to a set of agreements between a service provider and customer that define the scope, quality, and speed of the services being provided. As time passes, the SLA escalates the priority of the incident and leaves a marker as to its progress. SLAs are also used as a performance indicator for the service desk.

-   **Inactivity monitor**

    The inactivity monitor generates an event to prevent incidents from going unnoticed. When a certain amount of time has passed without an update to the incident, the event creates an email notification or triggers a script.


