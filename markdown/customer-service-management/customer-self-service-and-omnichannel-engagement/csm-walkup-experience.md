---
title: Walk-up Experience for Customer Service Management
description: The ServiceNow Walk-up Experience for Customer Service Management application enables you to set up a contact channel to support both online check-in and onsite check-in to a pre-established walk-up service center.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Walk-up Experience for Customer Service Management, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Walk-up Experience for Customer Service Management

The ServiceNow® Walk-up Experience for Customer Service Management application enables you to set up a contact channel to support both online check-in and onsite check-in to a pre-established walk-up service center.

Walk-up Experience aims to support users and significantly improve their satisfaction through a fast in-person support. Employees and business guests can get real-time, in-person help with their issues.

User personas and roles are defined as follows:

-   **Requesters**

    Users access the Walk-up Experience application in several ways.

    -   Online:
        -   Quickly check in online to the nearest available walk-up venue using the **Walk-up Check In** option on the Service Portal using your computer.

            **Note:** Walk-up Experience application automatically routes you to the nearest walk-up queue using the IP address of your computer. You can change the location, if desired.

        -   Join the queue and view your queue position.
        -   Schedule appointments for support and receive appointment reminders, as well as cancel or reschedule appointments from links in the reminder or from the online check-in interface.
        -   Schedule only one appointment per walk-up location queue at a time.

            **Note:** Even with a scheduled appointment, you can still check into a walk-up location queue online or in person onsite.

        -   Receive email notifications when your request is assigned to a technician when your position in the queue is close to being served and when your walk-up request has been closed or abandoned, should you decide not to attend the queue.
    -   Onsite at the Walk-up Experience location:
        -   Check into a queue at the physical walk-up location by manually entering your name, email, and contact details.
        -   Observe queue activities on a large monitor that displays both walk-in requesters and those with appointments.
        -   View the monitor displaying how many people are currently in the queue, guest positions in the queue, who is being served, and estimated wait times.
        -   Answer an available single-question survey which captures your user sentiment after a visit.
-   **Technicians or Agents**

    Customer support uses the Walk-up Experience application to meet the demand of urgent issues or requests from the requesters.

    -   Walk-up Experience technicians manage daily operations at the walk-up queue locations. They resolve customer service issues.
    -   Technicians can accept and close Walk-up Experience interactions through the Agent Workspace interface. Agent Workspace contains a personal inbox where walk-up interactions, if configured in Advanced Work Assignment, are automatically pushed for assignment.
    -   Agents can manage all aspects of Walk-up Experience fulfillment using Agent Workspace. Based on their capacity, and if records are on-hold, they can work on multiple transactions at the same time and promote interactions to cases.
    -   Technicians can view and accept scheduled appointments in their Agent Workspace personal inbox. Appointments are routed to the inbox according to agent availability. Alternatively, agents can pick and choose appointments manually.
    -   If necessary, technicians can work with anyone in the queue at any time. Technicians can manually assign themselves to a walk-up interaction, by accepting the interaction from a list of unassigned interactions in Agent Workspace.
-   **Managers**

    Managers supervise the walk-up location technicians and oversee daily operations.

    -   Walk-up managers can observe and capture operational and performance data by monitoring the walk-up dashboard.
    -   Walk-up managers can use the application to increase customer satisfaction, provide customer service in a timely manner, and report performance data to upper management.
-   **Administrators**

    Configure and maintain walk-up related systems, such as the walk-up location branding and text, queue locations and schedules, appointments, advanced work assignments, and notifications, and CSAT surveys.


|Role Name|Role|Description|
|---------|----|-----------|
|sn\_walkup.walkup\_login|Store representative|A user with this role helps requesters check in at the walk-up location.|
|sn\_csm\_walkup.walkup\_technician|CSM walk-up technician|A user with this role fulfills user demands at the CSM walk-up location.|
|sn\_csm\_walkup.walkup\_manager|CSM walk-up manager|A user with this role manages the team at the walk-up location.|
|sn\_csm\_walkup.walkup\_admin|CSM walk-up administrator|A user with this role administers walk-up interactions, location queues, and walk-up reasons.|

## Configuring Walk-up Experience for Customer Service Management

To get started with Walk-up Experience for Customer Service Management, see [Configure Walk-up Experience for Customer Service Management](../task/configure-walk-up-csm.md).

-   **[Walk-up Experience for guest users](csm-walkup-guest-store-app.md)**  
The Walk-up Experience application can enable guest users to manage walk-up appointments online from the Consumer Service Portal or Customer Service Portal home page.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

