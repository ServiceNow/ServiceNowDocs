---
title: OData Service Recommender AI agent
description: The OData Service Recommender AI agent identifies the most relevant OData service and endpoint from a populated service catalog, and can create a data model for the identified service if a model does not already exist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/now-assist-erp-ai-agent-odata-service-recommender.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 4
breadcrumb: [Use agentic AI, Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# OData Service Recommender AI agent

The OData Service Recommender AI agent identifies the most relevant OData service and endpoint from a populated service catalog, and can create a data model for the identified service if a model does not already exist.

## OData Service RecommenderAI agent overview

The OData Service Recommender AI agent helps you connect to SAP OData services without manually identifying endpoints or configuring data models. When you provide a description of the data you want to retrieve, the agent matches your intent against the descriptions in the OData service catalog and confirms the correct service and endpoint. You can also have the agent create a data model if an appropriate one does not already exist.

## Tools used by the OData Service Recommender AI agent

The OData Service Recommender AI agent uses six tools to complete its tasks:

-   **Scripts**

    Three scripts handle data retrieval and processing.

-   **Subflows**

    Two subflows manage the endpoint reading and data model creation steps.

-   **Web search**

    Web search interprets the description you enter and matches it against OData service catalog descriptions.


|Tool|Type|Description|
|----|----|-----------|
|Existing model checker|Script|Checks for existing OData models.|
|Model operation URL generator|Script|Forms a URL for navigating to an ERP model, optionally for a specific operation.|
|Read endpoints|Script|Reads all OData service endpoints from internal service catalog.|
|OData Service Checker|Subflow|Ensures that the given service is parsed into the Service catalog.|
|Model Creator|Subflow|Creates an OData model.|
|Use web search|Web search|This capability is a wrapper around searching, scraping and returns synthesized answer to search query.|

## Accessing the OData Service Recommender AI agent

Users with the sn\_aia\_admin role can access the workflow.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select the **AI agents** tab.
3.  Select **OData Service Recommender**.

    \[Omitted image "erp-odata-services-workflow-listing.jpg"\] Alt text: OData Service Recommender page with information about the workflow.

4.  Review the description, role, and steps. For more information, see [Define key requirements for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-key-requirements.md).
5.  Select **Continue** and review the tools that the OData Service Recommender AI agent uses. For more information, see [Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/add-tool-aia.md).
6.  Select **Continue** and view the user access options. For more information, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).
7.  Select **Continue** and view the data access options. For more information, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).
8.  Select **Continue** and view the trigger options. For more information, see [Add a trigger to an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/add-trigger-aw.md).
9.  Select **Continue** and view the channel and status options. For more information, see [Select channels and access for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/channels-access-aw.md).
10. Select **Save and test** to test the workflow. For more information, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/test-aia-use-case.md).

## Using the OData Service Recommender agentic workflow

The OData Service Recommender AI agent interprets your query, identifies the most relevant OData service and endpoint from the service catalog, and creates a data model if one does not already exist. Review the agent's recommendations before confirming to proceed.

**Note:** AI-generated recommendations may not be accurate in all cases. Verify the identified service and endpoint before confirming.

1.  Select the Now Assist icon \(\[Omitted image "now-assist-sparkle-icon-dark.png"\] Alt text:\) from anywhere in your instance to open the Now Assist panel.
2.  Ask for information in plain language. For example, `I’d like to connect to an OData service to read all sales orders`. Be as specific as possible about the data and the source system to improve the quality of the recommendation.

    \[Omitted image "erp-odata-services-ai-workflow1.jpg"\] Alt text: Now Assist panel with question typed in.

    The agent does the following:

    -   Identifies the service on the SAP system that most closely matches your request.
    -   Reads all available endpoints.
    -   Identifies the most appropriate CRUD operation.
    -   Displays a recommended service and endpoint.
    -   Checks if a data model for the identified service already exists.
    -   Waits for your confirmation before continuing.
3.  Review the recommendation.
4.  If an existing data model is found for the configuration, select the link provided to open the created data model. If no data model exists, go to the next step.
5.  If no data model exists and you'd like to create one, select **Yes** and follow the agent's guidance.

    \[Omitted image "erp-odata-services-ai-workflow2.jpg"\] Alt text: AI agent conversation asking if you want to create a data model with buttons for yes and no.

    The agent creates a data model with the correct endpoint and CRUD operation.

    \[Omitted image "erp-odata-services-ai-workflow3.jpg"\] Alt text: AI agent conversation with name, endpoint, and crud operation for the new OData data model.

6.  Select the link provided to open the created data model.
7.  Validate and confirm that the generated model meets your requirements.

**Note:** Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/find-ai-agents.md).

