---
title: Connect Workplace Reservation Management with Microsoft Teams
description: Establish connection between Microsoft Teams Communications and Workplace Reservation Management.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
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

1.  [Authenticate Microsoft Teams with Microsoft Azure](authenticate-microsoft-teams-with-micrsoft-azure.md).

2.  For Microsoft Teams, to create a meeting link on behalf of other users, refer to [Microsoft documentation](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy/).

3.  [Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md).

4.  [Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](setup-connectivity-between-servicenow-and-microsoft-teams-graph.md).

5.  [Create credential for Microsoft Teams Communication](create-credentials-for-microsoft-teams-connection.md).

6.  [Create connection and credential for Microsoft Teams Graph](create-connection-and-credentials-alias-for-microsoft-teams-graph.md).


1.  [Authenticate Microsoft Teams with Microsoft Azure](authenticate-microsoft-teams-with-micrsoft-azure.md)  
Set up authentication with Microsoft Azure to connect Microsoft Teams with Workplace Reservation Management application.
2.  [Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md)  
Register your Microsoft Teams Communications spoke with ServiceNow instance for OAuth authorization.
3.  [Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](setup-connectivity-between-servicenow-and-microsoft-teams-graph.md)  
Register your Microsoft Teams Graph with your ServiceNow® instance for OAuth authorization to get recordings after a virtual meeting.
4.  [Create credential for Microsoft Teams Communication](create-credentials-for-microsoft-teams-connection.md)  
Setup credentials for Microsoft Teams Communication spoke.
5.  [Create connection and credential for Microsoft Teams Graph](create-connection-and-credentials-alias-for-microsoft-teams-graph.md)  
Setup connection and credentials alias for Microsoft Teams Graph.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

