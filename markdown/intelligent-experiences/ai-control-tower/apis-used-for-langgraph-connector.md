---
title: APIs used for LangGraph connector
description: Explore the AWS APIs used in AI service Graph Connector for LangGraph.The table lists all the LangSmith API endpoints used by the connector.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 1
breadcrumb: [LangGraph, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# APIs used for LangGraph connector

Explore the AWS APIs used in AI service Graph Connector for LangGraph.The table lists all the LangSmith API endpoints used by the connector.

The following table lists all the LangSmith API endpoints used by the connector.

<table id="table_fq2_5kq_m3c"><tbody><tr><td>

API

</td><td>

Endpoint \(example\)

</td><td>

What it does

</td></tr><tr><td>

List Workspaces

</td><td>

https://api.smith.langchain.com /api/v1/workspaces/

</td><td>

Lists all workspaces at the given endpoint for the current API key or user

</td></tr><tr><td>

List Deployments

</td><td>

https://api.host.langchain.com/v2/deployments

</td><td>

Lists all agent deployments for a particular workspace

</td></tr><tr><td>

List Tracer Sessions

</td><td>

https://api.smith.langchain.com/api/v1/sessions

</td><td>

Lists all tracer sessions for a given workspace

</td></tr><tr><td>

Get Run Stats

</td><td>

https://api.smith.langchain.com /api/v1/runs/stats

</td><td>

Gets stats on a particular run, including LLM invocations

</td></tr></tbody>
</table>This table lists all the LangGraph Agent Deployment APIs used by the connector. The “endpoint\_url” below will be specific to each deployment and will be discovered at runtime by the app.

<table id="table_gjp_zkq_m3c"><tbody><tr><td>

API

</td><td>

Endpoint \(example\)

</td><td>

What it does

</td></tr><tr><td>

Search Assistants

</td><td>

\{\{endpoint\_url\}\}/assistants/search

</td><td>

Lists all assistants in each deployment

</td></tr><tr><td>

Search Threads

</td><td>

\{\{endpoint\_url\}\}/threads/search

</td><td>

Lists all threads for each deployment

</td></tr></tbody>
</table>