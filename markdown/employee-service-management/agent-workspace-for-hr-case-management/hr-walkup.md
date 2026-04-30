---
title: HR Walk-up
description: The HR Walk-up feature offers a convenient and efficient way for users to seek immediate assistance and support for their HR-related issues. With designated walk-up centers, users can seek in-person or remote assistance, report issues, and receive guidance from HR agents.Use HR walk-up to support HR requests raised by deskless workers.
locale: en-US
release: yokohama
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# HR Walk-up

The HR Walk-up feature offers a convenient and efficient way for users to seek immediate assistance and support for their HR-related issues. With designated walk-up centers, users can seek in-person or remote assistance, report issues, and receive guidance from HR agents.

**Note:** The HR Walk-up feature is available when the Walk-up Experience \(com.snc.walkup\) and Employee Center Pro \(sn\_ex\_sp\_pro\) plugins are installed.

-   **[Walk-up Experience](https://www.servicenow.com/docs/access?context=walkup-experience-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Walk-up Experience enhances user satisfaction and productivity by providing immediate and personalized support for IT-related needs.

    Every employee or a guest can check in and get support at an established walk-up service center.

-   **[Employee Center Pro Kiosk overview](../../employee-center/concept/deskless-kiosk-overview.md)**

    Employee Center Pro Kiosk enables all deskless workers with simplified access to information and services for self-serve and improved productivity.

    -   Access information and use services.
    -   Provide self-service options such as raising and tracking requests.

## HR Walk-up lists

HR Walk-up lists consist of the following categories:

<table id="table_mxc_bks_qdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Walk-up locations

</td><td>

HR agents can view a list of the walk-up queues they are assigned to support. Locations queues reveal all the information an HR agent must know to operate the queue efficiently.Select a location from the list to see the details, such as interactions, appointments, and reasons for visits.

</td></tr><tr><td>

Location kiosks

</td><td>

Location kiosks offer immediate assistance to the requesters by supporting them with technical issues, questions, or requests. The requesters can receive on-the-spot guidance or resolution for their HR-related problems.

</td></tr><tr><td>

Your assigned walk-ups

</td><td>

Interactions you assign to yourself when you accept an active interaction or that are assigned to you.HR agents assign interactions to themselves when they accept a queued interaction. Managers can assign interactions to specific HR agents.

</td></tr><tr><td>

Open-unassigned walk-ups

</td><td>

All open but unassigned interactions associated with your specific walk-up queue location. The interaction is Queued until an agent accepts it or is assigned the record.

</td></tr><tr><td>

Closed walk-ups

</td><td>

All Closed Complete and Closed Abandoned interactions assigned to a specific walk-up location queue. HR agents can abandon an interaction when a requester leaves the queue before receiving support.

</td></tr><tr><td>

Appointments

</td><td>

Walk-up appointment record that is created when a requester raised an appointment request from Employee Center.

</td></tr></tbody>
</table>## Use HR walk-up

Use HR walk-up to support HR requests raised by deskless workers.

### Before you begin

-   Role required: sn\_hr\_core.case\_writer
-   Verify that the Walk-up Experience \(com.snc.walkup\) and Employee Center Pro \(sn\_ex\_sp\_pro\) plugins are installed.
-   Employee must raise a walk-up appointment request. See [Plan your walk-up experience visit with Employee Center](https://www.servicenow.com/docs/access?context=plan-your-visit&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information. Based on the service and location, the appointment is assigned to an HR agent.

### Procedure

1.  Open HR Agent Workspace.

2.  From Lists, navigate to HR Walk-ups.

3.  From the HR walk-up appointments, select a walk-up appointment record.

    A read-only view of the walk-up appointment is displayed. From Attachments, you can download the outlook invite to your outlook calendar.

4.  Select **Open interaction**.

    Interaction record enables you to communicate with the requester. You can further create a case from the interaction based on your use case.

5.  To start working on the interaction, select **Accept**.

6.  To put the interaction on hold while you get additional information on the request, select **Put on Hold**.

7.  To cancel the interaction or appointment when a requester leaves the queue before receiving support, select **Abandon**.

    **Note:** Both the interaction and HR walk-up records are automatically closed when the requester cancels the request from Employee Center.


