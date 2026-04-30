---
title: Request Management in Service Operations Workspace
description: Service Operations Workspace for Request Management integrates the platform functionality for tier 1 agents into a multi-tab interface that helps agents efficiently manage multiple incidents, catalog requests, and catalog tasks.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Request Management in Service Operations Workspace

Service Operations Workspace for Request Management integrates the platform functionality for tier 1 agents into a multi-tab interface that helps agents efficiently manage multiple incidents, catalog requests, and catalog tasks.

As an agent, you can create a catalog request in Service Operations Workspace to initiate a catalog request flow from a different IT Service Management flow. For example, from an incident flow, you can create a request, and associate the request with the incident to help track requests associated with an incident and vice versa. You can also work on catalog tasks and update the state of the tasks, and manage approvals of requests and requested items.

The Service Operations Workspace ITSM Applications application \(sn-sow-itsm-cont\) that automatically installs the Request Management for Service Operations Workspace \(sn\_sow\_req\) application should be installed for the Request Management flows in Service Operations Workspace. For more information, see [Getting started with Service Operations Workspace for ITSM](getting-started-sow.md).

## Request Management categories in Service Operations Workspace

The following Request Management categories are available in Service Operations Workspace:

-   **Request**: Enables you to view active requests and requested items.
-   **Catalog Task**: Enables you to view the active tasks assigned to the current user and active tasks assigned to the current user’s assignment groups.

![Request Management categories in Service Operations Workspace](../image/sow-req-categories.png "Request Management categories")

## Request Management forms in Service Operations Workspace

The form layouts, UI actions, UI policies, and client scripts available on the following Request Management forms in the ServiceNow AI Platform UI are also available on the corresponding Service Operations Workspace forms.

-   Request
-   Request Item
-   Catalog Task

![Request form](../image/request-form-sow-polaris.png "Request form")

You can view the request form in Service Operations Workspace and track the record information like the request state, due date for a request, requested item.

You can view **Requested for** and **Opened by** cards in the record information panel.

-   **Requested for**: The **Requested for** card displays quick information about the requester, local time, department, location, info icon, and contact details. Additionally, you can select Recent requests to view the requests created by the requester and select the Assigned assets to view the assets assigned to the user.
-   **Opened by**: The **Opened by** card displays quick information about the requester, local time, department, location, info icon, and contact details.

You can also view the **Requested for** and **Opened by** cards in catalog task and request item.

![Request item form](../image/request-item-sow-polaris.png)

**Note:** A variable editor is displayed as a pop-up window for request items and catalog tasks only if it is included in the platform forms.

You can change the view of any Service Operations Workspace form by customizing the Service Operations Workspace view from the corresponding Request Management form in the ServiceNow AI Platform UI.

-   **[Create a catalog request in Service Operations Workspace](../task/create-catalog-request-sow.md)**  
Create a catalog request in Service Operations Workspace to initiate a catalog request flow from a different IT Service Management flow. For example, from an incident flow, you can create a request and associate the request with the incident to help track requests associated with an incident and vice versa.
-   **[View and approve records in Service Operations Workspace](../task/view-approvals-sow.md)**  
Access the My Approvals in SOW to manage the approval requests for change, request, catalog task, and requested item.

**Parent Topic:**[Operating IT services in your organization](enhancing-services-operations-in-organization.md)

**Related topics**  


[Play a guided tour in Service Operations Workspace](../task/play-guided-tour-sow.md)

[Add a user-specific quick link on the ITSM landing page](../task/add-quick-link.md)

[Create a list in Service Operations Workspace](../task/create-list-sow.md)

[Live Agent chat in Service Operations Workspace](configure-liveagent-sow.md)

[Interaction Management in Service Operations Workspace](interaction-sow.md)

[Incident Management in Service Operations Workspace](incident-sow.md)

[Change Management in Service Operations Workspace](change-sow.md)

