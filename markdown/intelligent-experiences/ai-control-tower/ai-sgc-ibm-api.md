---
title: APIs used by AI Service Graph Connector for IBM
description: Explore the IBM APIs used by the AI Service Graph Connector for IBM
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-sgc-ibm-api.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [IBM, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# APIs used by AI Service Graph Connector for IBM

Explore the IBM APIs used by the AI Service Graph Connector for IBM

The AI Service Graph Connector for IBM calls the following IBM APIs during discovery.

<table id="table_ns3_mf1_vjc" class="custom-rows"><thead><tr><th class="filter">

Method

</th><th>

API

</th><th>

IAM permission

</th><th>

Purpose

</th></tr></thead><tbody><tr><td colspan="4">

IBM watsonx Orchestrate

</td></tr><tr><td>

GET

</td><td>

https://resource-controller.cloud.ibm.com/v2/resource\_instances

</td><td>

Resource Controller Viewer

</td><td>

Discover all watsonx Orchestrate instances in the account.

</td></tr><tr><td>

GET

</td><td>

https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/orchestrate/agents

</td><td>

Orchestrate Reader

</td><td>

List all agents for an instance.

</td></tr><tr><td>

GET

</td><td>

https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/orchestrate/tools/toolId

</td><td>

Orchestrate Reader

</td><td>

Get details of each tool referenced by an agent.

</td></tr><tr><td>

POST

</td><td>

https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/traces/search

</td><td>

Orchestrate Reader

</td><td>

Search usage trace records \(cursor-paginated, separate scheduled import\).

</td></tr><tr><td>

POST

</td><td>

https://iam.cloud.ibm.com/identity/token

</td><td>

None

</td><td>

Exchange API Key for IAM Bearer token.

</td></tr><tr><td colspan="4">

IBM watsonx Runtime

</td></tr><tr><td>

GET

</td><td>

https://api.region.dataplatform.cloud.ibm.com/v2/spaces

</td><td>

Watson Studio Viewer

</td><td>

List all watsonx spaces per region.**Note:** For the us-south region, the API is `api.dataplatform.cloud.ibm.com/v2/spaces`.

</td></tr><tr><td>

GET

</td><td>

https://region.ml.cloud.ibm.com/ml/v4/deployments

</td><td>

WML Viewer

</td><td>

List all AI model deployments in a space \(paginated\).

</td></tr><tr><td>

GET

</td><td>

https://api.region.dataplatform.cloud.ibm.com/wx/v1/prompts/promptId

</td><td>

Watson Studio Reader

</td><td>

Get prompt template details, including model\_id and system prompt.**Note:** For the us-south region, the API is `api.dataplatform.cloud.ibm.com/wx/v1/prompts/promptId`.

</td></tr><tr><td>

POST

</td><td>

https://iam.cloud.ibm.com/identity/token

</td><td>

None

</td><td>

Exchange API Key for IAM Bearer token.

</td></tr></tbody>
</table>For the full API list and required IAM permissions, see the [AI Service Graph Connector for IBM — Setup Instructions \[KB2901071\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2901071) article in the Now Support Knowledge Base.

