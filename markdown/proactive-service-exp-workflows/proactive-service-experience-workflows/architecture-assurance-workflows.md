---
title: Proactive Service Experience Workflows architecture
description: There are multiple components that make up the architecture of the Proactive Service Experience Workflows application.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Product Support for Technology]
---

# Proactive Service Experience Workflows architecture

There are multiple components that make up the architecture of the Proactive Service Experience Workflows application.

The main components are as follows:

-   Flows and subflows
-   Escalation stages
-   Decision tables
-   Messages
-   Business rule
-   Client scripts
-   System properties
-   Roles
-   Assignment groups
-   Service Operations Workspace

## Decision tables

Based on the defined condition, Workflow Studio works with the Incident Escalation Policy \[sys\_hub\_flow\] decision table to determine which subflow to generate at certain escalation points.

## Messages

Each subflow in Proactive Service Experience Workflows is associated with a message file that provides instructions for agents to use to troubleshoot, escalate, and resolve network-initiated incidents. For more information about how to customize the default instructions for your internal troubleshooting processes, see [Customize message files](../task/configure-msg-file-taw.md).

## Roles

The `sn_ind_tsm_core.noc_agent` role is available with the Proactive Service Experience Workflows application. This role when added, ensures that the technical support agent can see the relevant information between ITSM and CSM applications. This role includes the following:

-   itil
-   wm\_initiator
-   wm\_read
-   sn\_customerservice.case\_viewer
-   sn\_customerservice.customer\_data\_viewer

Several assignment groups are included with this role and other groups can also have the admin role. The `sn_ind_tsm_sdwan.ticket_integrator` role can be used for trouble tickets created from the TMF 621 Open API use cases.

## Proactive Service Experience Workflows process

The following diagram shows the steps involved in the Proactive Service Experience Workflows process:

![Proactive Service Experience Workflows End-to-end process](../image/psew-workflow-graphic.png)

-   **[Enhancing customer impact visibility for PSEW processes](enhance-customer-impact-visibility-psew-process.md)**  
Use the customer impact tab to reduce navigation time, and enhance tracking and management of PSEW processes. This visibility enables you to quickly assess business impact and take informed actions.

**Parent Topic:**[Exploring the Product Support for Technology](explore-assurance-workflows.md)

