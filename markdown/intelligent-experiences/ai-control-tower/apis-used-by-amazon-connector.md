---
title: APIs used by Microsoft- Azure &amp; Copilot
description: Explore the AWS APIs used in AI service Graph Connector for Amazon.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# APIs used by Microsoft- Azure &amp; Copilot

Explore the AWS APIs used in AI service Graph Connector for Amazon.

The table lists all the Amazon API endpoints used by the connector.

## New Azure Foundry — Discovery &amp; Usage

<table id="table_pv1_zxq_m3c"><tbody><tr><td>

API

</td><td>

Endpoint

</td><td>

What it does

</td></tr><tr><td>

List Projects

</td><td>

[https://management.azure.com/subscriptions/\{subscription\_id\}/resourceGroups/\{resource\_group\}/providers/Microsoft.CognitiveServices/accounts?api-version=2025-06-01&amp;kind=Project](https://management.azure.com/subscriptions/%7Bsubscription_id%7D/resourceGroups/%7Bresource_group%7D/providers/Microsoft.CognitiveServices/accounts?api-version=2025-06-01&kind=Project)

</td><td>

Lists all Azure AI Foundry projects in a resource group

</td></tr><tr><td>

List Deployments

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/deployments?api-version=v1](https://resource_name.services.ai.azure.com/api/projects/project_name/deployments?api-version=v1)

</td><td>

Lists all model deployments within a Foundry project

</td></tr><tr><td>

List Agents

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/agents?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/agents?api-version=2025-11-15-preview)

</td><td>

Lists all agents in a Foundry project

</td></tr><tr><td>

List Agent Versions

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/agents/agent\_name/versions?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/agents/agent_name/versions?api-version=2025-11-15-preview)

</td><td>

Lists all versions of a specific agent

</td></tr><tr><td>

List conversations

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/openai/conversations?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/openai/conversations?api-version=2025-11-15-preview)

</td><td>

Lists all conversation threads in a Foundry project

</td></tr><tr><td>

List Conv Items

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/openai/conversations/conv\_id/items?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/openai/conversations/conv_id/items?api-version=2025-11-15-preview)

</td><td>

Lists all messages/items within a specific conversation

</td></tr></tbody>
</table>## AI Services \(Classic\)

<table id="table_v12_11r_m3c"><tbody><tr><td>

API

</td><td>

Endpoint

</td><td>

What it does

</td></tr><tr><td>

List Projects

</td><td>

[https://management.azure.com/subscriptions/\{subscription\_id\}/resourceGroups/\{resource\_group\}/providers/Microsoft.CognitiveServices/accounts?api-version=2025-06-01&amp;kind=Project](https://management.azure.com/subscriptions/%7Bsubscription_id%7D/resourceGroups/%7Bresource_group%7D/providers/Microsoft.CognitiveServices/accounts?api-version=2025-06-01&kind=Project)

</td><td>

Lists all AI Services projects in a resource group

</td></tr><tr><td>

List Deployments

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/deployments?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/deployments?api-version=2025-11-15-preview)

</td><td>

Lists all model deployments within a project

</td></tr><tr><td>

List Assistants

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/assistants?api-version=v1](https://resource_name.services.ai.azure.com/api/projects/project_name/assistants?api-version=v1)

</td><td>

Lists all assistants \(agents\) in a project List

</td></tr><tr><td>

List Threads

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/threads?limit=limit&amp;api-version=v1](https://resource_name.services.ai.azure.com/api/projects/project_name/threads?limit=limit&api-version=v1)

</td><td>

Lists all execution threads in a project

</td></tr></tbody>
</table>## ML Services \(AI Hub\)

<table id="table_jx3_lcr_m3c"><tbody><tr><td>

API

</td><td>

Endpoint

</td><td>

**What it does**

</td></tr><tr><td>

List Subscriptions

</td><td>

[https://management.azure.com/subscriptions?api-version=management\_api\_version](https://management.azure.com/subscriptions?api-version=management_api_version)

</td><td>

Lists all Azure subscriptions available to the authenticated principal

</td></tr><tr><td>

List Resource Group

</td><td>

[https://management.azure.com/subscriptions/subscription\_id/resourceGroups?api-version=management\_api\_version](https://management.azure.com/subscriptions/subscription_id/resourceGroups?api-version=management_api_version)

</td><td>

Lists all resource groups within a subscription

</td></tr><tr><td>

List MLWorkspaces

</td><td>

[https://management.azure.com/subscriptions/%7Bsubscription\_id%7D/resourceGroups/%7Bresource\_group%7D/providers/Microsoft.MachineLearningServices/workspaces?api-version=2023-04-01](https://management.azure.com/subscriptions/%7Bsubscription_id%7D/resourceGroups/%7Bresource_group%7D/providers/Microsoft.MachineLearningServices/workspaces?api-version=2023-04-01)

</td><td>

Lists all Azure ML workspaces in a resource group

</td></tr><tr><td>

List Deployments

</td><td>

[https://resource\_name.services.ai.azure.com/api/projects/project\_name/deployments?api-version=2025-11-15-preview](https://resource_name.services.ai.azure.com/api/projects/project_name/deployments?api-version=2025-11-15-preview)

</td><td>

Lists all model deployments within an ML project

</td></tr><tr><td>

List Assistants from ML Services

</td><td>

[https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription\_id/resourceGroups/resource\_group/providers/Microsoft.MachineLearningServices/workspaces/workspace\_name/assistants?api-version=v1](https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription_id/resourceGroups/resource_group/providers/Microsoft.MachineLearningServices/workspaces/workspace_name/assistants?api-version=v1)

</td><td>

Lists all agents/assistants from an AzureML workspace

</td></tr><tr><td>

List Threads from ML Service

</td><td>

[https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription\_id/resourceGroups/resource\_group/providers/Microsoft.MachineLearningServices/workspaces/workspace\_name/threads?api-version=v1](https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription_id/resourceGroups/resource_group/providers/Microsoft.MachineLearningServices/workspaces/workspace_name/threads?api-version=v1)

</td><td>

Lists all threads from an AzureML workspace

</td></tr><tr><td>

List Thread Runs from ML Service

</td><td>

[https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription\_id/resourceGroups/resource\_group/providers/Microsoft.MachineLearningServices/workspaces/workspace\_name/threads/thread\_id/runs?api-version=v1](https://region.api.azureml.ms/agents/v1.0/subscriptions/subscription_id/resourceGroups/resource_group/providers/Microsoft.MachineLearningServices/workspaces/workspace_name/threads/thread_id/runs?api-version=v1)

</td><td>

Lists all thread runs within a specific thread in an AzureML workspace

</td></tr></tbody>
</table>## AWS APIs used for Copilot

<table id="table_jnz_xcr_m3c"><tbody><tr><td>

API

</td><td>

Endpoint

</td><td>

Description

</td></tr><tr><td>

List of all the agents in the Copilot environment

</td><td>

&lt;org-url&gt;/api/data/v9.2/bots

</td><td>

Returns metadata about all Copilot Studio bots \(agents\) registered in a Dataverse environment, including their name, status, authentication config, and ownership details. This is the primary endpoint to discover and inventory deployed copilots.

</td></tr><tr><td>

List of all the components per agent

</td><td>

&lt;org-url&gt;/api/data/v9.2/botcomponents

</td><td>

Exposes the internal authoring components of a Copilot, such as topics, entities, variables, and trigger phrases, stored in the botcomponent table. Essential for inspecting or programmatically analyzing a bot's conversational logic and structure.

</td></tr><tr><td>

List Conversations

</td><td>

&lt;org url&gt;/api/data/v9.2/conversationtranscripts

</td><td>

Retrieves the full chat/conversation transcripts between users and Copilot Studio bots, stored in the Dataverse conversationtranscript table.

</td></tr></tbody>
</table>