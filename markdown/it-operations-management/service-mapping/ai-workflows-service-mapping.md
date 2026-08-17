---
title: AI in Service Mapping
description: AI-powered features in Service Mapping help administrators automate service map creation, connect business applications to discovered services, and query live service topology using natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/ai-workflows-service-mapping.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-07-08"
reading_time_minutes: 3
keywords: [Now Assist, generative AI, Service Mapping, AI agent, agentic workflow, MCP Server, service map]
breadcrumb: [Service Mapping, ITOM Visibility, IT Operations Management]
---

# AI in Service Mapping

AI-powered features in Service Mapping help administrators automate service map creation, connect business applications to discovered services, and query live service topology using natural language.

Service Mapping includes several AI-powered features. All features require ServiceNow Otto for IT Operations Management \(ITOM\) to be installed.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## AI agents and agentic workflows

Service Mapping AI agents and agentic workflows automate service map creation, business application mapping, and change impact analysis.

<table id="table_ai-workflows-service-mapping"><thead><tr><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Service Mapping AI Agent

</td><td>

Autonomously creates service maps from ML-powered Application Service Candidates \(ASCs\). The agent evaluates candidates, filters noise such as monitoring clients and operating system processes, and creates the service topology in the CMDB.

</td><td>

A Service Mapping administrator wants to process a large volume of ML-powered candidates and create service maps automatically, without reviewing each candidate individually.

</td><td>

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Business App Mapping AI Agent

</td><td>

Automatically creates CSDM "Uses::Used by" relationships between Business Applications and discovered Application Services using AI semantic search.

</td><td>

A Service Mapping administrator wants to connect discovered application services to their business application context in the CSDM without manually mapping each relationship.

</td><td>

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Analyze potential impact agentic workflow

</td><td>

Analyzes how a change request might affect relevant servers and services. The agent verifies prerequisites, retrieves the change request, selects up to 10 affected servers, identifies matches with suggested services, and displays an impact analysis in the ServiceNow Otto panel. The analysis is also saved to the change request work notes. Uses the Service Mapping Candidate and Service Mapping Candidates Impact skills.

</td><td>

An operator or change manager wants to assess the risk of a change request before approving it, without manually reviewing all affected CIs.

</td><td>

-   [Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Assess a change request with the Analyze potential impact workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/use-now-assist-analyze-impact-agentic-workflow.md)
-   [Activate the Service Mapping Candidate skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidate-skill.md)
-   [Activate the Service Mapping Candidates Impact skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/activate-sm-candidates-impact-skill.md)

</td></tr></tbody>
</table>-   **[Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/now-assist-itom-analyze-potential-impact-workflow.md)**  
The Analyze potential impact agentic workflow analyzes how a change request might impact servers and services. This analysis helps you make informed decisions about the next steps regarding the change request.
-   **[AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-ai-specialists.md)**  
The Service Mapping AI agents automate the creation and maintenance of service maps in the Configuration Management Database \(CMDB\), reducing manual effort for Service Mapping administrators.

**Parent Topic:**[Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_ServiceMappingOverview.md)

