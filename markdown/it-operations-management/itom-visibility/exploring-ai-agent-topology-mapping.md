---
title: Exploring AI Agent Topology Mapping
description: Learn how AI Agent Topology Mapping discovers AI infrastructure components across cloud platforms using patterns.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [AI Agent Topology Mapping, ITOM Visibility, IT Operations Management]
---

# Exploring AI Agent Topology Mapping

Learn how AI Agent Topology Mapping discovers AI infrastructure components across cloud platforms using patterns.

## AI Agent Topology Mapping overview

AI Agent Topology Mapping extends the pattern-based discovery framework to identify and track AI-specific components in your environment. The application uses patterns to discover AI components from cloud platforms, populating the CMDB with configuration items \(CIs\). This approach provides centralized visibility into your AI infrastructure alongside traditional IT assets. For more information about how patterns work, see [Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md).

AI Agent Topology Mapping discovers the following AI components:

-   AI Agents: Intelligent entities that perform tasks and orchestrate AI workflows
-   AI Models: Foundational models that power AI capabilities, such as large language models
-   AI Prompts: Instructions and configurations that guide agent behavior and responses

## AI Agent Topology Mapping users

The following user roles have access to patterns or pattern-related modules and can perform various actions. Note that customizing patterns requires basic knowledge of programming.

<table id="table_mj5_2tg_23c"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discovery admin

</td><td>

Can view, create, edit, and publish patterns. The role enables users to run discovery, migrate probes or CAPI to patterns, and access discovery logs and dashboards.

</td></tr><tr><td>

PD user

</td><td>

Has read-only access to **Discovery Pattern Log**.

</td></tr><tr><td>

PD admin

</td><td>

Can view, create, edit, and publish patterns.

</td></tr><tr><td>

PDE viewer

</td><td>

Starting with Pattern Designer Enhancements version 3.9.0, users can view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer can view the **Command Validation Tool** modules and related tables, but doesn't have permissions to modify or edit them.

The pde\_viewer role can view the following tables only:

-   Command List \[pd\_command\_list\]
-   Command Validation Task \[pd\_command\_validation\]
-   Command Validation Task Results \[pd\_command\_validation\_results\]
-   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
-   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]

For more information, see [Discovery commands for probes and patterns](../../discovery/concept/discovery-command-probe-pattern.md).

</td></tr><tr><td>

PD MID

</td><td>

Not assigned to a user directly but to the MID Server record or the user under which the MID Server runs. The role enables the MID Server to interpret and run pattern-based probes.

</td></tr><tr><td>

MID Server

</td><td>

Can grant the MID Server access to the instance.

</td></tr></tbody>
</table>## AI Agent Topology Mapping workflow

The following workflow describes how a discovery administrator uses AI Agent Topology Mapping to discover and track AI infrastructure components.

1.  Install AI Agent Topology Mapping patterns from the ServiceNow Store.
2.  Configure cloud credentials with appropriate permissions for AI platforms.
3.  Create or update discovery schedules for environments containing AI resources.
4.  Run discovery to identify AI components and populate the CMDB.
5.  View discovered AI agents, models, and prompts in CMDB and non-CMDB tables.
6.  Monitor discovery logs to verify successful pattern execution.
7.  Schedule recurring discovery to maintain up-to-date AI infrastructure inventory.

## AI Agent Topology Mapping benefits

|Benefit|Description|
|-------|-----------|
|Centralized AI infrastructure visibility|Visibility into AI agents, models, and prompts alongside other IT assets in the CMDB, supporting AI Control Tower outcomes.|
|Automated discovery|Patterns automatically discover AI agents from supported cloud platforms during scheduled runs and populate the CMDB.|
|Multi-cloud support|Discovery of AI resources across multiple cloud platforms using a single application.|
|Security and compliance|Tracking of AI component versions and configurations to help maintain governance and compliance requirements for AI deployments.|
|Vulnerability management|Tracking of AI component versions and dependencies to identify security risks.|
|Change impact analysis|Near real-time visibility into AI agent dependency and topology relationships to support ITSM and AIOps use cases.|
|Business context and service mapping|Discovered AI assets serve as the foundation for building tag-based service maps aligned with the Common Service Data Model \(CSDM\).|

## What to explore next

To learn more about configuring and using AI Agent Topology Mapping, see:

-   [Configuring AI Agent Topology Mapping](configuring-ai-agent-topology-mapping.md)
-   [AI Agent Topology Mapping reference](../reference/ai-agent-topology-mapping-reference.md)

