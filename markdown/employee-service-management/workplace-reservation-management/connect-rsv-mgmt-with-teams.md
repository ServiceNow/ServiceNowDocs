---
title: Connect Workplace Reservation Management with Microsoft Teams
description: Establish connection between Microsoft Teams Communications and Workplace Reservation Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/connect-rsv-mgmt-with-teams.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Connect Workplace Reservation Management with Microsoft Teams

Establish connection between Microsoft Teams Communications and Workplace Reservation Management.

## Before you begin

Ensure that the following plugins are installed:

-   Microsoft Teams Communications spoke \(for creating meeting links\)
-   Microsoft Teams Graph Spoke \(to get recordings\)
-   Workplace Reservation Management

Role required: admin

## Procedure

1.  [Authenticate Microsoft Teams with Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/authenticate-microsoft-teams-with-micrsoft-azure.md).

2.  For Microsoft Teams, to create a meeting link on behalf of other users, refer to [Microsoft documentation](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy/).

3.  [Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md).

4.  [Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-microsoft-teams-graph.md).

5.  [Create credential for Microsoft Teams Communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-credentials-for-microsoft-teams-connection.md).

6.  [Create connection and credential for Microsoft Teams Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-connection-and-credentials-alias-for-microsoft-teams-graph.md).


1.  [Authenticate Microsoft Teams with Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/authenticate-microsoft-teams-with-micrsoft-azure.md)  
Set up authentication with Microsoft Azure to connect Microsoft Teams with Workplace Reservation Management application.
2.  [Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md)  
Register your Microsoft Teams Communications spoke with ServiceNow instance for OAuth authorization.
3.  [Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-microsoft-teams-graph.md)  
Register your Microsoft Teams Graph with your ServiceNow® instance for OAuth authorization to get recordings after a virtual meeting.
4.  [Create credential for Microsoft Teams Communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-credentials-for-microsoft-teams-connection.md)  
Setup credentials for Microsoft Teams Communication spoke.
5.  [Create connection and credential for Microsoft Teams Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-connection-and-credentials-alias-for-microsoft-teams-graph.md)  
Setup connection and credentials alias for Microsoft Teams Graph.

**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Zoom]()

[Display permanent seat assignments on floor maps]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

