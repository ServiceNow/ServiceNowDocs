---
title: Automatically route information requests using Advanced Work Assignment
description: Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign information requests, such as public records requests, to designated agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Information Request Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Automatically route information requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign information requests, such as public records requests, to designated agents.

The Information Request Playbook application provides the following items that are used in AWA to automatically route and assign public sector information requests:

-   **Information Request service channel** - The default service channel for routing incoming public sector information requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Information Request assignment group** - The default assignment group that identifies the agents handling public sector information requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector Information Requests queue** - The default queue to which public sector information requests are routed.
-   **Inbox layouts** - The default card layouts for information request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Information Request layout: Includes **Short description**, **Constituent**, and **Service** fields.
    -   Business Information Request layout: Includes **Short description**, **Business**, **Business Contact**, and **Service** fields.
    -   Generic Information Request layout: Includes **Short description** and **Service** fields.

As an admin, you can enable and disable Advanced Work Assignment for Information Request cases, as well as change the default attributes for the Information Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Information Requests service channel](../task/psds-awa-configure-ir.md).

