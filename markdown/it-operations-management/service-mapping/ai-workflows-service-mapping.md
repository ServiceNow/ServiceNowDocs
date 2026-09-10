---
title: AI in Service Mapping
description: AI-powered features in Service Mapping help administrators automate service map creation, connect business applications to discovered services, and query live service topology using natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/ai-workflows-service-mapping.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-04-09"
reading_time_minutes: 4
keywords: [Now Assist, Otto, Service Mapping, AI]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# AI in Service Mapping

AI-powered features in Service Mapping help administrators automate service map creation, connect business applications to discovered services, and query live service topology using natural language.

Service Mapping includes several AI-powered features. All features require ServiceNow Otto for IT Operations Management \(ITOM\) to be installed.

**Note:** Depending on your license, you have access to certain application features, generative AI skills, agentic workflows, and AI agents.

## MCP servers

The Service Mapping MCP server exposes instance data to external AI clients through the Model Context Protocol, giving those clients structured, ACL-enforced access to live application service data.

<table id="table_sm-mcp-servers"><thead><tr><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Service Mapping MCP server

</td><td>

Exposes five read-only tools through the CMDB MCP Server. The tools give AI clients such as Claude structured access to live application service data, including full service topology, server impact graphs, and unmapped CIs. Authentication uses OAuth 2.0 with JWT tokens and enforces the same ACLs as standard instance API calls.

</td><td>

A Service Mapping administrator or operator wants to query service topology, identify mapping gaps, or assess server impact. They do so by using natural language in an AI client, without navigating the instance UI.

</td><td>

-   [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)
-   [Activate the CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-mcp-server.md)
-   [Connect Claude Desktop to the Service Mapping MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/connect-claude-desktop-sm-mcp.md)
-   [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md)

</td></tr></tbody>
</table>## AI agents and agentic workflows

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

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Business App Mapping AI Agent

</td><td>

Automatically creates CSDM "Uses::Used by" relationships between Business Applications and discovered Application Services using AI semantic search.

</td><td>

A Service Mapping administrator wants to connect discovered application services to their business application context in the CSDM without manually mapping each relationship.

</td><td>

-   [AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-ai-specialists.md)
-   [Activate AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-ai-specialists.md)

</td></tr><tr><td>

Analyze potential impact agentic workflow

</td><td>

Analyzes how a change request might affect relevant servers and services. The agent verifies prerequisites, retrieves the change request, selects up to 10 affected servers, identifies matches with suggested services, and displays an impact analysis in the ServiceNow Otto panel. The analysis is also saved to the change request work notes. Uses the Service Mapping Candidate and Service Mapping Candidates Impact skills.

</td><td>

An operator or change manager wants to assess the risk of a change request before approving it, without manually reviewing all affected CIs.

</td><td>

-   [Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Assess a change request with the Analyze potential impact workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/use-now-assist-analyze-impact-agentic-workflow.md)
-   [Activate the Service Mapping Candidate skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/activate-sm-candidate-skill.md)
-   [Activate the Service Mapping Candidates Impact skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/activate-sm-candidates-impact-skill.md)

</td></tr></tbody>
</table>-   **[AI Agents for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-ai-specialists.md)**  
The Service Mapping AI agents automate the creation and maintenance of service maps in the Configuration Management Database \(CMDB\), reducing manual effort for Service Mapping administrators.
-   **[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)**  
The Service Mapping tools expose live application service data and enable AI clients to query service topology, identify mapping gaps, and create application services in natural language.

**Parent Topic:**[Using Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/using-service-mapping.md)

