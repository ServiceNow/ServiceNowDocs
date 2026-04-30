---
title: Automatically route service requests using Advanced Work Assignment
description: Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign public sector service requests, such as non-emergency requests, to designated agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Automatically route service requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign public sector service requests, such as non-emergency requests, to designated agents.

The Service Request Playbook application provides the following items that are used in AWA to automatically route and assign public sector service requests:

-   **Service Requests service channel** - The default service channel for routing incoming public sector service requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Requests assignment group** - The default assignment group that identifies the agents handling public sector service requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Service Requests queue** - The default queue to which public sector service requests are routed.
-   **Inbox layouts** - The default card layouts for service request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Service Request layout: Includes **Short description**, **Constituent**, and **Service** fields.
    -   Business Service Request layout: Includes **Short description**, **Business**, **Business Contact**, and **Service** fields.
    -   Generate Service Request Layout: Displayed when anonymous users submit service requests. Includes **Short description** and **Service** fields

As an admin, you can enable and disable Advanced Work Assignment for Service Request cases, as well as change the default attributes for the Service Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Service Requests service channel](../task/psds-awa-configure.md).

