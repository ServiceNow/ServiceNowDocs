---
title: Automatically route social benefit requests using Advanced Work Assignment
description: Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign social benefits requests to designated agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Social Benefits Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Automatically route social benefit requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign social benefits requests to designated agents.

The Social Benefits Playbook application provides the following items that are used in AWA to automatically route and assign social benefits requests:

-   **Social Benefits Request service channel** - The default service channel for routing incoming public sector social benefits requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Social Benefits Request assignment group** - The default assignment group that identifies the agents handling public sector social benefits requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector Social Benefits Requests queue** - The default queue to which public sector social benefits requests are routed.
-   **Inbox layouts** - The default card layouts for social benefits request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Social Benefits Layout: Includes **Short description**, **Constituent**, and **Case Type** fields.
    -   Business Social Benefits Layout: Includes **Short description**, **Business**, **Business Contact**, and **Case Type** fields.

As an admin, you can enable and disable Advanced Work Assignment for Social Benefits Request cases, as well as change the default attributes for the Social Benefits Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Social Benefit Requests service channel](../task/psds-awa-configure-sbp.md).

