---
title: Requirements for using AI in Zero Copy Connector for ERP
description: Before you use ServiceNow Otto in Zero Copy Connector for ERP, confirm that your instance has the required license, plugins, and roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [erp, zero, copy, connector, sap, ai, otto, require, prerequisite, license, plugin, role, erp\_ai\_user]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Requirements for using AI in Zero Copy Connector for ERP

Before you use ServiceNow Otto in Zero Copy Connector for ERP, confirm that your instance has the required license, plugins, and roles.

## Zero Copy Connector for ERP setup

AI capabilities in Zero Copy Connector for ERP depend on an installed Zero Copy Connector for ERP application and a connected ERP system. For more information, see [Requirements for installing Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-installation.md) and [Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/install-erp-integration.md).

## Licensing

The ERP data discovery and ERP data query skills require a Workflow Data Fabric Pro license.

## Plugins

<table id="table_erp-ai-prereq-plugins"><thead><tr><th>

Plugin

</th><th>

ID

</th><th>

Required for

</th></tr></thead><tbody><tr><td>

ServiceNow Otto for Zero Copy Connector

</td><td>

sn\_erp\_ai

</td><td>

All ServiceNow Otto skills, agentic workflows, and AI agents in Zero Copy Connector for ERP

</td></tr><tr><td>

Knowledge Graph

</td><td>

After activating any ServiceNow generative AI application, the following are installed by default: -   Graph QL plugin \(com.glide.graphql\)
-   Knowledge Graph application \(sn\_kg\)

</td><td>

The Explore ERP models agentic workflow and the OData Service Recommender AI agent

</td></tr></tbody>
</table>For more information, see [Install the AI plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md).

## Roles

|Role|Required to|
|----|-----------|
|sn\_erp\_integration.erp\_ai\_user|Required to use generative AI and agentic AI in Zero Copy Connector for ERP|
|sn\_erp\_integration.erp\_admin|Complete AI-assisted tasks that change models|
|admin|Install the plugin, activate and deactivate skills, and set skill access|

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Additional setup for agentic workflows and AI agents

Before you use the Explore ERP models agentic workflow or the OData Service Recommender AI agent, complete the following setup:

-   ServiceNow Otto for Virtual Agent and the ServiceNow Otto panel are on.
-   The **Otto Q&amp;A**, **Otto Topics**, and **AI agents** conversational skills are activated in ServiceNow Otto for Virtual Agent.
-   A large language model \(LLM\) provider is set, with at least one active connection.

For the steps, see [Prepare ServiceNow Otto for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.md).

**Parent Topic:**[Configuring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.md)

