---
title: Using agentic workflows in ServiceNow Otto for CMDB
description: Users with the sn\_cmdb\_user role can access several ServiceNow Otto for CMDB agentic workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-07-13"
reading_time_minutes: 5
breadcrumb: [ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Using agentic workflows in ServiceNow Otto for CMDB

Users with the sn\_cmdb\_user role can access several ServiceNow Otto for CMDB agentic workflows.

## Agentic workflows

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

<table id="table_lxk_lck_h2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Create configuration item

</td><td>

Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow promotes that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI. For more information, see [Create a CI using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-creator.md)

</td><td>

CI creator

</td></tr><tr><td>

Provide advice on CMDB governance

</td><td>

Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to help users to trust the data that they use for their work. For more information, see [Getting advice from ServiceNow Otto on CMDB governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-governance.md).

</td><td>

-   CMDB data manager
-   CMDB data certification and attestation manager
-   CMDB data ownership manager
-   CMDB health metrics manager
-   CMDB life cycle manager
-   CMDB principal class manager

</td></tr><tr><td>

Search CMDB

</td><td>

The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CIs of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query. For more information, see [Use ServiceNow Otto to search the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md).

</td><td>

CI search

</td></tr></tbody>
</table>**Note:**

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

## Running AI agents autonomously

**Important:** By default, all agentic workflow and AI agent records are read only.

To run the AI agents autonomously, you must first duplicate the agentic workflow and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

-   **[Create a CI using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-creator.md)**  
The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.
-   **[Getting advice from ServiceNow Otto on CMDB governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-governance.md)**  
Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to help users to trust the data that they use for their work.
-   **[Business application candidate agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-c.md)**  
The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.
-   **[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)**  
The Assess CMDB impact agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.
-   **[Use ServiceNow Otto to search the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md)**  
The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CIs of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query.
-   **[Recommend service graph connector agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-suggest-sgc-mappings.md)**  
Sometimes you're not sure which integration to use to capture CI data. When you provide ServiceNow Otto with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

**Parent Topic:**[ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)

