---
title: AI in Zero Copy Connector for ERP
description: ServiceNow Otto helps you find ERP data, identify SAP objects, and build and run ERP models in Zero Copy Connector for ERP when you describe what you need in plain language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/ai-in-zero-copy-connector-for-erp.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 7
keywords: [erp, zero, copy, connector, sap, ai, otto, generative, skill, agentic, ai agent]
breadcrumb: [Exploring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# AI in Zero Copy Connector for ERP

ServiceNow Otto helps you find ERP data, identify SAP objects, and build and run ERP models in Zero Copy Connector for ERP when you describe what you need in plain language.

## ServiceNow Otto in Zero Copy Connector for ERP overview

The ServiceNow Otto for Zero Copy Connector plugin \(sn\_erp\_ai\) adds generative AI skills, an agentic workflow, and an AI agent to Zero Copy Connector for ERP. Instead of looking up SAP tables, BAPIs, OData services, or RFCs manually, you ask ServiceNow Otto in plain language and confirm the result.

Use AI to complete the following work:

-   Query SAP standard database tables for data and transactional records.
-   Identify the SAP objects to use when you create an ERP model or model operation.
-   Find and create an OData data model without identifying the endpoint yourself.
-   Find and run a configured ERP model.

Every AI-assisted task in Zero Copy Connector for ERP also has a manual path. If ServiceNow Otto is unavailable or a skill is deactivated, complete the same work by using the manual task.

## AI capabilities in Zero Copy Connector for ERP

|Capability|Type|What it does|Where you use it|
|----------|----|------------|----------------|
|[ERP data discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-query-sap-data-with-erp-data-discovery.md)|Skill|Queries SAP standard database tables and returns matching data and transactional records, such as purchase orders, sales orders, billing documents, and deliveries. Use it to list records or to monitor exceptions, such as blocked deliveries or rejected items.|ServiceNow Otto panel|
|[ERP data query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-identify-sap-objects-with-erp-data-query.md)|Skill|Identifies the SAP objects, such as tables, BAPIs, and OData endpoints, that you need to query the data you describe. Use it to create ERP models and model operations faster.|ServiceNow Otto panel|
|[Explore ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-run-a-model-with-explore-erp-models.md)|Agentic workflow|Answers questions about configured ERP database tables and models, including models in ERP content packs, and runs a model that you name. The workflow uses the ERP data fetcher, ERP action invoker, and ERP output formatter AI agents.|ServiceNow Otto panel|
|[OData Service Recommender](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-create-odata-model-with-odata-service-recommender.md)|AI agent|Identifies the most relevant SAP OData service and endpoint from the service catalog, checks for an existing data model, and creates a data model if one doesn't exist.|ServiceNow Otto panel|

## When AI is available

AI capabilities in Zero Copy Connector for ERP depend on an installed Zero Copy Connector for ERP application and a connected ERP system.

-   **Skills**: The ERP data discovery and ERP data query skills are available after you install and activate the ServiceNow Otto for Zero Copy Connector plugin. The skills require a Workflow Data Fabric Pro license.

    **Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

-   **Agentic workflows and AI agents**: The Explore ERP models agentic workflow and the OData Service Recommender AI agent also require the Knowledge Graph plugin and additional setup. For more information, see [Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md).

The sn\_erp\_integration.erp\_ai\_user role is required to use generative AI and agentic AI in Zero Copy Connector for ERP.

Tasks that change models also require the sn\_erp\_integration.erp\_admin role.

To open the ServiceNow Otto panel, select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance.

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-pickers.md).\)

To install the plugin and activate skills, see [Install the ServiceNow Otto for Zero Copy Connector plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md).

## Agentic workflow and AI agent records

**Important:** By default, all agentic workflow and AI agent records are read-only.

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-controls-aia.md).

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/find-ai-agents.md).

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some AI products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some AI products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some AI products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Troubleshoot and get help

-   [Troubleshoot ServiceNow Otto agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-troubleshoot-otto-skills-and-agentic-workflows.md)
-   [ServiceNow Community on AI and Intelligence](https://www.servicenow.com/community/now-assist/ct-p/now-assist)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect information about applications \(and associated application files\) in which app generation was utilized. Customers can opt out of future data collection at any time, as described in the [AI Opt-Out page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

**Parent Topic:**[Exploring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/exploring-erp-integration.md)

