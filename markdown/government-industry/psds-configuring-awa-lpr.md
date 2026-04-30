---
title: Automatically route license and permit requests using Advanced Work Assignment
description: Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license/permit requests to designated agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Automatically route license and permit requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license/permit requests to designated agents.

The License and Permit Playbook application provides the following items that are used in AWA to automatically route and assign license/permit requests:

-   **License and Permit Request service channel** - The default service channel for routing incoming public sector license/permit requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector License and Permit Request assignment group** - The default assignment group that identifies the agents handling public sector license/permit requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector License and Permit Requests queue** - The default queue to which public sector license/permit requests are routed.
-   **Inbox layouts** - The default card layouts for license/permit request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent License/Permit Layout: Includes **Short description**, **Constituent**, and **Case Type** fields.
    -   Business License/Permit Layout: Includes **Short description**, **Business**, **Business Contact**, and **Case Type** fields.

As an admin, you can enable and disable Advanced Work Assignment for License/Permit Request cases, as well as change the default attributes for the License/Permit Requests service channel, such as the related assignment group and queue settings. For details, see [Configure License and Permits Requests service channel](../task/psds-awa-configure-lpr.md).

