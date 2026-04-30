---
title: Work item reorder errors in EAP Backlog
description: Review the scenarios when the reordering of work items can fail in the Backlog of Enterprise Agile Planning workspace.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Work item reorder errors in EAP Backlog

Review the scenarios when the reordering of work items can fail in the Backlog of Enterprise Agile Planning workspace.

While reordering work items in different sections of the EAP Backlog, the reorder can fail due to an error in the ranking configuration. Following are the scenarios where reordering of work items can fail:

-   **Scenario 1: Global ranking plugin is not active**

    Check if the Global Ranking Application plugin \(com.snc.sdlc.ranking\) is active in your ServiceNow instance. If not, contact your admin to activate it.

-   **Scenario 2: Work item doesn't have a rank configuration**

    Check if all the work items that you are reordering have a rank configuration. If not, contact your admin to update rank configuration for these work item types.

-   **Scenario 3: Target row doesn't have a global rank**

    Check if the work item before or after your target position to reorder has a global rank. If not, contact your system admin to generate a global rank for them.


**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

