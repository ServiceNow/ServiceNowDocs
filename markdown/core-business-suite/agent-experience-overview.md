---
title: Agent Experience
description: Core Business Suite Agent Experience provides a unified dashboard for agents managing work across multiple business units, designed for organizations where one agent handles multiple areas.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/agent-experience-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [agent experience, unified dashboard, agent workspace, fulfiller]
breadcrumb: [Use, Core Business Suite]
---

# Agent Experience

Core Business Suite Agent Experience provides a unified dashboard for agents managing work across multiple business units, designed for organizations where one agent handles multiple areas.

Agent Experience consolidates work items from different Core Business Suite business units into a single interface. Agents can efficiently manage tasks, approvals, and cases across HR, Finance, Procurement, and other business areas without switching between multiple dashboards.

## Target users

Agent Experience is designed for organizations that assign one agent to manage multiple business units. Instead of having dedicated agents for HR, Finance, and other departments, a single agent can handle work across all Core Business Suite business units.

## Key capabilities

Agent Experience provides the following capabilities:

-   Unified view of work items across all Core Business Suite business units
-   Quick snapshot of workload status including pending approvals and SLA risks
-   Direct approval actions from the dashboard
-   Filtering and sorting options to prioritize work
-   Integration with ITSM incidents when installed
-   Customizable canvas with additional platform widgets

## Technical architecture

Agent Experience runs off-platform but remains accessible through your instance URL at `https://<instance-name>.service-now.com/cbshome/home`. The application uses a separate server accessed through the load balancer.

## Widgets

Agent Experience includes three widgets specific to Core Business Suite:

-   **On Your Plate**

    Provides a snapshot of your current workload including cases, tasks, and approvals from Core Business Suite business units

-   **Approvals**

    Displays pending approvals and lets you approve or reject items directly from the widget

-   **My Work**

    Shows a comprehensive list of assigned work items with filtering, sorting, and search capabilities


Additional widgets from the ServiceNow platform are available and can be added to the canvas.

-   **[Agent Experience widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/agent-experience-widgets.md)**  
Core Business Suite Agent Experience includes three widgets that help agents view and manage their workload: On Your Plate, Approvals, and My Work.
-   **[Access Agent Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/access-agent-experience.md)**  
Access the Agent Experience dashboard to view and manage your work items across Core Business Suite business units.
-   **[Filter and sort work items in My Work widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/filter-sort-work-items.md)**  
Use filtering and sorting options in the My Work widget to organize and prioritize your work items in Agent Experience.
-   **[Configure Agent Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/configure-agent-experience.md)**  
Configure Agent Experience to customize the dashboard for your organization.

**Parent Topic:**[Using Core Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/cbs-using-parent.md)

