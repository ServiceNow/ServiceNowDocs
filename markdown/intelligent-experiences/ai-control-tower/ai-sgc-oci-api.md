---
title: APIs used by AI Service Graph Connector for OCI
description: Explore the OCI APIs used by the AI Service Graph Connector for OCI
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-sgc-oci-api.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [OCI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# APIs used by AI Service Graph Connector for OCI

Explore the OCI APIs used by the AI Service Graph Connector for OCI

The AI Service Graph Connector for OCI calls the following OCI APIs during discovery.

|Method|API|IAM permission|Purpose|
|------|---|--------------|-------|
|OCI Generative AI|
|GET|https://identity.*region*.oraclecloud.com/20160918/compartments?compartmentId=*compartmentId*&amp;compartmentIdInSubtree=true&amp;lifecycleState=ACTIVE|inspect compartments|List active compartments within discovery scope.|
|GET|https://identity.*region*.oraclecloud.com/20160918/compartments/*compartmentId*|inspect compartments|Test connection.|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/models?compartmentId=*compartmentId*|read generative-ai-family|List base and custom models.|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/importedModels?compartmentId=*compartmentId*|read generative-ai-family|List imported models.|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/endpoints?compartmentId=*compartmentId*|read generative-ai-family|List endpoints.|
|OCI Generative AI Agents|
|GET|https://identity.*region*.oraclecloud.com/20160918/compartments?compartmentId=*compartmentId*&amp;compartmentIdInSubtree=true&amp;lifecycleState=ACTIVE|inspect compartments|List active compartments within discovery scope.|
|GET|https://identity.*region*.oraclecloud.com/20160918/compartments/*compartmentId*|inspect compartments|Test connection.|
|GET|https://agent.generativeai.*region*.oci.oraclecloud.com/20240531/agents?compartmentId=*compartmentId*|read genai-agent-family|List AI agents.|
|GET|https://agent.generativeai.*region*.oci.oraclecloud.com/20240531/tools?compartmentId=*compartmentId*&amp;agentId=*agentId*|read genai-agent-family|List tools for a specific agent.|
|GET|https://agent.generativeai.*region*.oci.oraclecloud.com/20240531/agentEndpoints?compartmentId=*compartmentId*|read genai-agent-family|List agent endpoints \(used for usage metrics collection\).|
|GET|https://agent.generativeai.*region*.oci.oraclecloud.com/20240531/agentEndpoints/*agentEndpointId*|read genai-agent-family|Get agent endpoint details \(agent-as-tool resolution\).|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/models/*modelId*|read generative-ai-family|Get model details \(resolve agent-referenced models\).|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/endpoints/*endpointId*|read generative-ai-family|Get model endpoint details \(resolve agent-referenced endpoints to backing models\).|
|POST|https://telemetry.*region*.oraclecloud.com/20180401/metrics/actions/summarizeMetricsData|read metrics|Retrieve agent usage metrics.|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/importedModels/*modelId*|read generative-ai-family|Get imported model details \(resolve agent-referenced imported models\).|
|GET|https://generativeai.*region*.oci.oraclecloud.com/20231130/endpoints?compartmentId=*compartmentId*|read generative-ai-family|List endpoints.|

For the full API list and required IAM permissions, see the [Service Graph Connector for OCI - Setup Instructions \[KB2898105\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2898105) article in the Now Support Knowledge Base.

