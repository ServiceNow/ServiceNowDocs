---
title: Create an OData data model with the OData Service Recommender AI agent
description: ServiceNow Otto finds the SAP OData service and endpoint that match the data you describe and creates a data model for it if one doesn't already exist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-create-odata-model-with-odata-service-recommender.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 3
keywords: [erp, zero, copy, connector, sap, odata, service, endpoint, model, ai, ai agent, otto, recommender]
breadcrumb: [ERP models, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Create an OData data model with the OData Service Recommender AI agent

ServiceNow Otto finds the SAP OData service and endpoint that match the data you describe and creates a data model for it if one doesn't already exist.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

The ServiceNow Otto for Zero Copy Connector and Knowledge Graph plugins are installed. For more information, see [Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md).

ServiceNow Otto is set up for AI agents. For more information, see [Prepare ServiceNow Otto for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.md).

## About this task

When you describe the data that you want, the OData Service Recommender AI agent matches your request against the descriptions in the OData service catalog. It recommends a service, an endpoint, and a CRUD operation, and then checks whether a data model for that service already exists.

**Note:** AI-generated recommendations may not be accurate in all cases. Verify the service and endpoint before you confirm.

## Procedure

1.  Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

2.  Describe the data that you want in plain language.

    For example, `I’d like to connect to an OData service to read all sales orders`. Be as specific as possible about the data and the source system to improve the recommendation.

    The AI agent displays a recommended service and endpoint, and tells you whether a data model for that service already exists.

3.  Review the recommended service, endpoint, and CRUD operation.

4.  Choose how to continue.

    -   If a data model already exists, select the link to open it.
    -   If no data model exists, select **Yes** to have the AI agent create one, and follow its guidance.
    If you selected **Yes**, the AI agent creates a data model with the recommended endpoint and CRUD operation and provides a link to it.

5.  Select the link to open the data model, and check that it meets your requirements.


## Result

You have an OData data model that you can manage in Model Manager.

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

## Create the model manually

If ServiceNow Otto is unavailable or the AI agent is deactivated, create an OData connection, add a data model, and then add an OData entity to a model operation. For more information, see [Create an OData connection in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/create-an-odata-connection.md), [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md), and [Add an OData entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-an-odata-entity-to-a-model-operation.md).

## What to do next

Set up the inputs for the model. For more information, see [Manage input parameters for a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs.md).

**Parent Topic:**[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)

**Related topics**  


[OData service recommender AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/zcc-odata-service-recommender-ai-agent.md)

[Skills, agentic workflows, and AI agents in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-ai-skills-workflows-and-agents.md)

[Connecting Zero Copy Connector for ERP to ERP using OData](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-use-odata-and-http-connection.md)

