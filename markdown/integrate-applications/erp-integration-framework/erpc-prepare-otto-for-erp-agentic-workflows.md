---
title: Prepare ServiceNow Otto for agentic workflows and AI agents
description: Turn on ServiceNow Otto for Virtual Agent and activate the required conversational skills. Confirm an active LLM connection before you use the Explore ERP models agentic workflow or the OData Service Recommender AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [erp, zero, copy, connector, ai, otto, agentic, ai agent, virtual agent, llm, connection, prerequisite]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Prepare ServiceNow Otto for agentic workflows and AI agents

Turn on ServiceNow Otto for Virtual Agent and activate the required conversational skills. Confirm an active LLM connection before you use the Explore ERP models agentic workflow or the OData Service Recommender AI agent.

## Before you begin

Role required: admin

The ServiceNow Otto for Zero Copy Connector and Knowledge Graph plugins are installed. For more information, see [Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md).

## About this task

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Procedure

1.  Check that ServiceNow Otto for Virtual Agent and the ServiceNow Otto panel are on.

    For more information, see [Configuring Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ci-configuring.md) and [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).

2.  Activate the required conversational skills in ServiceNow Otto for Virtual Agent.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

    2.  Select **Manage assistants**.

    3.  Select **ServiceNow Otto for Virtual Agent**.

    4.  In the left side menu, select **Otto skills**.

    5.  Activate **Otto Q&amp;A**, **Otto Topics**, and **AI agents** if they aren't already active.

3.  Set a large language model \(LLM\) provider.

    For information about available providers and how to set one, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/manage-large-language-models.md).

4.  Check that your LLM provider has at least one active connection.

    1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Select the alias for your LLM provider.

    3.  Select the **Connections** tab.

        At least one connection has **Active** set to **true**.

        \[Omitted image "erp-data-explorer-workflow4.png"\] Alt text: Connection and credential alias record with the Connections tab showing one active connection.

    If no connection is active, create one or activate an existing one. For more information, see [Get started with connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/connection-information.md).


## Result

Users with the sn\_erp\_integration.erp\_ai\_user role can use the Explore ERP models agentic workflow and the OData Service Recommender AI agent from the ServiceNow Otto panel.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.md)

