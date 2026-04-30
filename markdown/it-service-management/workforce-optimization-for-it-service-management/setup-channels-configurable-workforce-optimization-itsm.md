---
title: Setting up Channels in Workforce Optimization for ITSM
description: Set up service channels, queues, and key performance indicators \(KPIs\) to route work items automatically to agents based on an agent's availability, capacity, and skills.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Setting up Channels in Workforce Optimization for ITSM

Set up service channels, queues, and key performance indicators \(KPIs\) to route work items automatically to agents based on an agent's availability, capacity, and skills.

With Workforce Optimization for ITSM:

-   As a channel administrator, you can set up service channels and work item queues and then automatically route incoming work to agents. You can also configure real-time refresh intervals for the metrics and lists so that managers can always see the latest information about their teams.
-   As a manager, you can view the real-time operational metrics for the work that is being done by your teams and the specific items that your teams are working on.

**Note:** As an administrator, you can configure filters to refine the search and view targeted results. Filters are persisted across all channel management pages in the session. To view a list of the default interactive filters and the KPI reports for channels, queues, agents, and groups that you can map to the interactive filters, see [the filter configuration tables for Channels](../task/configure-filter-configurable-manager-workspace.md). By default, the assignment group filter is applied to all lists and groups that you manage. You can disable interactive filters by using the **sn\_channel\_mgmt.filter\_config.enable** property.

-   **[Add service channels and queues](../task/add-channels-queues-configurable-wfo-itsm.md)**  
Add service channels and queues to automatically route incoming work items to agents.
-   **[Create assignment rules and groups](../task/create-assignment-rules-configurable-wfo-itsm.md)**  
Define agent assignment rules and specify groups of agents who are eligible to receive overflow work assignments for a queue.
-   **[Configure KPIs for service channels](../task/configure-kpis-service-channels-configurable-wfo-itsm.md)**  
Configure key performance indicators in service channels to track the ongoing work and real-time performance of your teams.
-   **[Configure KPIs for agents](../task/configure-kpis-agents-configurable-wfo-itsm.md)**  
Configure key performance indicators \(KPIs\) in service channels for your agents so that you can track the agents' ongoing work and real-time performance.
-   **[Configure KPIs for queues](../task/configure-kpis-queues-configurable-wfo-itsm.md)**  
Configure key performance indicators in queues to track the incoming work for specific categories of work in a service channel.
-   **[Configure supervisor lists for service channels](../task/configure-lists-channels-configurable-wfo-itsm.md)**  
Configure supervisor lists in a service channel to view the list of active work items across service channels and queues.
-   **[Schedule the generation of a daily report](../task/schedule-report-configurable-wfo-itsm.md)**  
Generate and distribute a daily scheduled report that summarizes the agent's work performance via email.
-   **[Channel Management extension point in Workforce Optimization for ITSM](../reference/extension-points-channels-sort-order-wfo-itsm.md)**  
Use extension points to call scripts to configure the list sort order in Channel Management.

**Parent Topic:**[Channels in Workforce Optimization for ITSM](exploring-channels-configurable-workforce-optimization-itsm.md)

