---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) Smart Actions for Telecom agentic workflow
description: Use the Smart Actions for Telecom agentic workflow to retrieve customer data and get a summary with a recommended next action for a customer account or consumer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-smart-actions-agentic-workflow.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-07-31"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) Smart Actions for Telecom agentic workflow

Use the Smart Actions for Telecom agentic workflow to retrieve customer data and get a summary with a recommended next action for a customer account or consumer.

## Smart Actions for Telecom agentic workflow overview

Retrieve a consolidated view of customer data using the Smart Actions for Telecom agentic workflow. When triggered from the Recommended Actions panel on the Telecom Customer 360 page, the workflow retrieves data for the current customer account or consumer. The workflow delivers a Customer 360 summary in the ServiceNow Auto panel and performs the following steps:

-   Retrieves customer account or consumer context and performs a pre-diagnostic check across product inventory, duplicate cases, open incidents, open work orders, active alerts, and outstanding billing. The workflow uses the Telecom Customer Enterprise Graph to enrich customer context at runtime, retrieving service-related data such as service problem cases and sold product details. For more information, see [Telecom Customer Enterprise Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-telecom-customer-enterprise-graph.md).
-   Delivers a Customer 360 summary with an overall risk assessment and a recommended next action.
-   Remains available to answer follow-up questions using the gathered context, the knowledge graph, or the associated tools.

The Smart Actions for Telecom agentic workflow supports these tables:

-   Customer account
-   Consumer

Role required: `sn_tmt_agentic_ai.smart_actions_agent`

**Note:** The Smart Actions for Telecom agentic workflow is available in read-only mode. Before using the workflow, you must make a copy and adjust the settings according to your requirements. See [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md) for details.

## Role masking

Required role: `sn_tmt_agentic_ai.smart_actions_agent`

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Access the Smart Actions for Telecom agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Smart Actions for Telecom**.

To create an agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## Test the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Smart Actions for Telecom**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents used in the Smart Actions for Telecom agentic workflow

The following AI agent is used to execute the instructions for the agentic workflow.

To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

|AI agent|AI agent role|
|--------|-------------|
|Telecom Smart Actions Agent|Gathers full telecom customer context from a triggering account or consumer record. Performs a pre-diagnostic check across product inventory, the knowledge graph, duplicate cases, open incidents, open work orders, active alerts, and outstanding billing. Does not diagnose network faults. Remains available to answer follow-up questions after the initial run.|

**Related topics**  


[Telecom Customer Enterprise Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-telecom-customer-enterprise-graph.md)

