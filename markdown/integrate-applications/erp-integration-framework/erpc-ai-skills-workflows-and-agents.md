---
title: Skills, agentic workflows, and AI agents in Zero Copy Connector for ERP
description: ServiceNow Otto in Zero Copy Connector for ERP includes two skills, one agentic workflow, and one standalone AI agent. Each one has a matching task to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-ai-skills-workflows-and-agents.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 3
keywords: [erp, zero, copy, connector, sap, ai, otto, skill, agentic, ai agent, reference, erp\_ai\_user]
breadcrumb: [Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Skills, agentic workflows, and AI agents in Zero Copy Connector for ERP

ServiceNow Otto in Zero Copy Connector for ERP includes two skills, one agentic workflow, and one standalone AI agent. Each one has a matching task to use.

The sn\_erp\_integration.erp\_ai\_user role is required to use generative AI and agentic AI in Zero Copy Connector for ERP.

For the full list of license, plugin, and role requirements, see [Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md). For details about the role, see [Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-roles.md).

<table id="table_erp-ai-ref-capabilities"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th><th>

Components

</th></tr></thead><tbody><tr><td>

[ERP data discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-query-sap-data-with-erp-data-discovery.md)

</td><td>

Skill

</td><td>

Queries SAP standard database tables and returns matching data and transactional records, such as purchase orders, sales orders, billing documents, and deliveries.

</td><td>

None

</td></tr><tr><td>

[ERP data query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-identify-sap-objects-with-erp-data-query.md)

</td><td>

Skill

</td><td>

Identifies the SAP objects, such as tables, BAPIs, and OData endpoints, that you need to query the data you describe.

</td><td>

None

</td></tr><tr><td>

[Explore ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-run-a-model-with-explore-erp-models.md)

</td><td>

Agentic workflow

</td><td>

Answers questions about configured ERP database tables and models, including models in ERP content packs, and runs a model that you name.

</td><td>

-   [ERP action invoker AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-erp-action-invoker-ai-agent.md)
-   [ERP data fetcher AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-erp-data-fetcher-ai-agent.md)
-   [ERP output formatter AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-erp-output-formatter-ai-agent.md)

</td></tr><tr><td>

[OData Service Recommender](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-create-odata-model-with-odata-service-recommender.md)

</td><td>

AI agent

</td><td>

Identifies the most relevant OData service and endpoint, and creates a data model for the service if a model doesn't already exist.

</td><td>

For details, see [OData service recommender AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-odata-service-recommender-ai-agent.md).

</td></tr></tbody>
</table>**Note:** By default, all agentic workflow and AI agent records are read-only.

## Role masking

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-controls-aia.md).

## Standalone AI agents

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/find-ai-agents.md).

**Parent Topic:**[Zero Copy Connector for ERP reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-reference.md)

**Related topics**  


[AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/ai-in-zero-copy-connector-for-erp.md)

[Zero Copy Connector for ERP AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-ai-agents-overview.md)

