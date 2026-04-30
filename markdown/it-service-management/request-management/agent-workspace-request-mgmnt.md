---
title: Agent Workspace for Request Management
description: Agent Workspace for Request Management integrates the platform functionality specific to tier 1 agents into an easy-to-navigate interface. This multi-tab interface helps the agents to efficiently manage multiple incidents, catalog requests, and catalog tasks. The ITSM Workspace plugin \(com.snc.agent\_workspace.itsm\) that automatically activates the Service Catalog - Workspace \(com.glideapp.servicecatalog.workspace\) plugin should be activated for the Request Management flows in workspace.
locale: en-US
release: yokohama
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request Management, IT Service Management]
---

# Agent Workspace for Request Management

Agent Workspace for Request Management integrates the platform functionality specific to tier 1 agents into an easy-to-navigate interface. This multi-tab interface helps the agents to efficiently manage multiple incidents, catalog requests, and catalog tasks. The ITSM Workspace plugin \(com.snc.agent\_workspace.itsm\) that automatically activates the Service Catalog - Workspace \(com.glideapp.servicecatalog.workspace\) plugin should be activated for the Request Management flows in workspace.

## Request Management categories in workspace

-   **Request**: Displays the active requests and requested items.
-   **Catalog Task**: Displays the active tasks assigned to the current user, and to at least one of the assignment groups of the user.

## Request Management forms in workspace

The form layouts, UI actions, UI policies, and client scripts that are available on the following Request Management forms in Platform are also available on the corresponding Workspace forms.

-   Request
-   Request Item
-   Catalog Task

**Note:** A variable editor is displayed as a pop-up window for request items and catalog tasks only if it is included in the Platform forms.

If you want to change the view of any workspace form, customize the workspace view from the corresponding request management form in the platform UI.

-   **[Create a catalog request in Agent Workspace](../task/create-request-workspace.md)**  
You can create a catalog request in Agent Workspace to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.

**Parent Topic:**[Request Management](../../planning-and-policy/concept/c_RequestManagement.md)

