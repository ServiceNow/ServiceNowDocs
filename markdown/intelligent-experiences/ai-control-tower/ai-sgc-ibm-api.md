---
title: APIs used by AI Service Graph Connector for IBM
description: Explore the IBM APIs used by the AI Service Graph Connector for IBM
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-ibm-api.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [IBM, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# APIs used by AI Service Graph Connector for IBM

Explore the IBM APIs used by the AI Service Graph Connector for IBM

The AI Service Graph Connector for IBM calls the following IBM APIs during discovery.

|Method|API|IAM permission|Purpose|
|------|---|--------------|-------|
|IBM watsonx Orchestrate|
|GET|https://resource-controller.cloud.ibm.com/v2/resource\_instances|Resource Controller Viewer|Discover all watsonx Orchestrate instances in the account.|
|GET|https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/orchestrate/agents|Orchestrate Reader|List all agents for an instance.|
|GET|https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/orchestrate/tools/toolId|Orchestrate Reader|Get details of each tool referenced by an agent.|
|POST|https://api.region.watson-orchestrate.cloud.ibm.com/instances/instanceGuid/v1/traces/search|Orchestrate Reader|Search usage trace records \(cursor-paginated, separate scheduled import\).|
|POST|https://iam.cloud.ibm.com/identity/token|None|Exchange API Key for IAM Bearer token.|
|IBM watsonx Runtime|
|GET|https://api.region.dataplatform.cloud.ibm.com/v2/spaces|Watson Studio Viewer|List all watsonx spaces per region.|
|GET|https://region.ml.cloud.ibm.com/ml/v4/deployments|WML Viewer|List all AI model deployments in a space \(paginated\).|
|GET|https://api.region.dataplatform.cloud.ibm.com/wx/v1/prompts/promptId|Watson Studio Reader|Get prompt template details, including model\_id and system prompt.|
|POST|https://iam.cloud.ibm.com/identity/token|None|Exchange API Key for IAM Bearer token.|

For the full API list and required IAM permissions, see the [AI Service Graph Connector for IBM — Setup Instructions \[KB2901071\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2901071) article in the Now Support Knowledge Base.

