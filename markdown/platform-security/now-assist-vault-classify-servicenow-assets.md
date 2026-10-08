---
title: Classifying ServiceNow assets with Vault agents agentic workflow
description: The Classify assets with ServiceNow Vault agent recommends a data class for each ServiceNow column in the Data Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/now-assist-vault-classify-servicenow-assets.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Classifying ServiceNow assets with Vault agents agentic workflow

The Classify assets with ServiceNow Vault agent recommends a data class for each ServiceNow column in the Data Catalog.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Data class recommendations for ServiceNow assets

Data classification gives you visibility into the types of data hosted on your instance and supports compliance with privacy laws and industry regulations. Classifying columns manually is inconsistent between reviewers and doesn't scale to customer estates of many thousands of tables. Use this agentic workflow to recommend a data class for each column in scope, with a reason for each recommendation.

When you install ServiceNow Otto for Vault on an instance that has the ServiceNow Data Catalog Governance \(Scope: sn\_dcg\_app\) application, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

## ServiceNow assets and enterprise assets

The Data Catalog in Workflow Data Fabric collects table and column definitions from connected data sources and stores them as data assets. Definitions collected from a ServiceNow source come from the Dictionary Entries \[sys\_dictionary\] table, which defines every table and field in the system. For more information, see [ServiceNow metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/servicenow-metadata-collector.md).

Data assets are grouped by origin. Assets collected from a ServiceNow source are ServiceNow assets, and assets collected from any other source are enterprise assets. This agentic workflow classifies ServiceNow assets only.

Recommendations are based on schema metadata: the table name and label, the column name and label, the dictionary entry, any existing classifications, and the name and description of the application that owns the table.

The workflow recommends from the data classes already defined on your instance rather than from a fixed set, so recommendations reflect your own classification model.

## Classify ServiceNow assets

Recommend and apply data classes for the ServiceNow columns in the Data Catalog. Role required: dcg\_data\_privacy\_admin

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Classify assets with ServiceNow Vault**.

**Note:** You can invoke this agentic workflow using one of the following methods:

-   In the ServiceNow Otto panel, enter a prompt such as `Classify my ServiceNow assets` or `Recommend data classes for columns in the Data Catalog`.
-   In the Workflow Data Fabric panel, select this agentic workflow from the available options.

For the procedure, see [Classify ServiceNow assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/classify-servicenow-assets-now-assist-vault.md).

## AI agents used in the classifying ServiceNow assets with Vault agents agentic workflow

|Name|Description|
|----|-----------|
|Classify assets with ServiceNow Vault|Uses various tools to retrieve ServiceNow assets from the Data Catalog, recommend a data class for each column, and apply the recommendations that you confirm.|

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/find-ai-agents.md).

-   **[Classify ServiceNow assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/classify-servicenow-assets-now-assist-vault.md)**  
Run the Classify assets with ServiceNow Vault agent to get a recommended data class for each ServiceNow column in the Data Catalog, review the recommendations, and apply them.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/use-now-assist-vault-agentic-ai.md)

