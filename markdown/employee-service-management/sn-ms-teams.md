---
title: IT Service Management integration with Microsoft Teams and Microsoft 365
description: IT Service Management integration with Microsoft Teams extends the Now Virtual Agent integration with Microsoft Teams to enable employees to more effectively request and receive service from within Microsoft Teams.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration for Employee Experience, Explore, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# IT Service Management integration with Microsoft Teams and Microsoft 365

IT Service Management integration with Microsoft Teams extends the Now Virtual Agent integration with Microsoft Teams to enable employees to more effectively request and receive service from within Microsoft Teams.

## Functionalities of the IT Service Management integration with Microsoft Teams

The IT Service Management integration with Microsoft Teams application includes the following additional capabilities:

-   Actionable notifications: For approval and comments on tickets. Users can reply on the notifications from within Microsoft Teams.
    -   Approval – for Request \(single Requested Item\), Change Request
    -   Ticket comments: Employees are able to respond to notifications on the tickets from within Microsoft Teams: Incident, Requested Item, and Change Request.
-   Agents can initiate a Microsoft Teams chat with an employee from an incident, change request, or request item. Agents can then copy the chat transcript back to the ticket as a comment.
-   Additional informational notifications for:
    -   Incident: Resolved, Updated
    -   Requested Item: Completed, Approved, Rejected, Updated
    -   Approval \(for all approvals other than Request \(with a single requested item\), and Change Request\)

**Note:** Approvals with e-Signature are not yet supported for IT Service Management integration with Microsoft Teams.

|Feature|License Requirements|
|-------|--------------------|
|Actionable Notifications|ITSM Pro|
|Chat - Agent to Employee/Agent to Agent|ITSM Standard or above|
|Employee Center|ITSM Standard or above|

## Using the IT Service Management integration with Microsoft Teams

You must perform the following activities to integrate IT Service Management with Microsoft Teams in your ServiceNow instance:

1.  [Install IT Service Management integration with Microsoft Teams application](../task/install-sn-ms-teams-plugin.md)
2.  [Setting up the ServiceNow instance for Microsoft Teams integration](setup-tenants.md)

To configure the IT Service Management integration with Microsoft Teams in your ServiceNow instance, see [Configure IT Service Management integration with Microsoft Teams](sn-ms-teams-config-it.md).

To manage the IT Service Management integration with Microsoft Teams in your ServiceNow instance, see [Customize IT Service Management integration with ServiceNow](customize-sn-ms-teams.md).

To use the IT Service Management integration with Microsoft Teams in your ServiceNow instance, see [Use ITSM and HRSD integrations with Microsoft Teams](user-sn-ms-teams.md).

**Parent Topic:**[Explore Microsoft Teams and Microsoft 365 integration for Employee Experience](c_employee_experience.md)

**Related topics**  


[HR Service Delivery integration with Microsoft Teams and Microsoft 365](sn-ms-teams-hr.md)

[Universal Request integration with Microsoft Teams](sn-ms-teams-ur.md)

