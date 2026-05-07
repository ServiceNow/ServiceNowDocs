---
title: APIs used by Salesforce
description: Explore the APIs used in AI Service Graph Connector for Salesforce.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Salesforce, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# APIs used by Salesforce

Explore the APIs used in AI Service Graph Connector for Salesforce.

The following table lists all the Salesforce API endpoints used by the connector.

<table id="table_nvx_qx3_43c"><tbody><tr><td>

API

</td><td>

Endpoint

</td><td>

What it does

</td></tr><tr><td>

Bot Definition, BotVersion

</td><td>

https://&lt;domain\_name&gt;.salesforce.com/services/data/v65.0/query?q=SELECT Fields\(ALL\), \(SELECT Id, VersionNumber, Status FROM BotVersions\) FROM BotDefinition WHERE Type != 'Bot' LIMIT 100 OFFSET 100

</td><td>

Fetch all AI Agents created in Salesforce.

</td></tr><tr><td>

Configured Einstein Models

</td><td>

https://&lt;domain\_name&gt;.salesforce.com/services/data/v65.0/ssot/machine-learning/configured-models/

</td><td>

Fetch Models configured in Salesforce Einstein Studio

</td></tr><tr><td>

GenAiFunctionDefinition

</td><td>

https://&lt;domain\_name&gt;.salesforce.com/services/data/v65.0/query?q=SELECT id, DeveloperName, Description, IsConfirmationRequired, Plugin.Planner.Id, Plugin.Planner.DeveloperName, Plugin.DeveloperName, Plugin.MasterLabel, Plugin.Id, Plugin.Description, Plugin.Scope from GenAiFunctionDefinition WHERE PluginId != null LIMIT 100 OFFSET 100

</td><td>

Fetch all the tools details used by AI Agents

</td></tr><tr><td>

GenAiPluginDefinition, GenAiPluginInstructionDef

</td><td>

https://&lt;domain\_name&gt;.salesforce.com//services/data/v65.0/query?q=SELECT MasterLabel,DeveloperName, SortOrder, Description,id,GenAiPluginDefinition.DeveloperName,GenAiPluginDefinition.Id,GenAiPluginDefinition.Description,GenAiPluginDefinition.Scope, GenAiPluginDefinition.MasterLabel, GenAiPluginDefinition.Planner.DeveloperName FROM GenAiPluginInstructionDef LIMIT 100 OFFSET 100

</td><td>

Fetch all prompts information associated or used by AI Agents

</td></tr><tr><td>

ConversationDefinitionId, ConversationDefinitionEventLog

</td><td>

https://&lt;domain\_name&gt;.salesforce.com/services/data/v65.0/query?q=SELECT ParentId, User, MIN\(EventDateTime\) Timestamp, ConversationDefinitionId, COUNT\(Id\) TotalInvocations FROM ConversationDefinitionEventLog WHERE LogType = 'InputMessage' GROUP BY ParentId, CreatedById, ConversationDefinitionId, User ORDER BY MIN\(EventDateTime\) DESC

</td><td>

Fetch Usage Information for AI Agents.

</td></tr></tbody>
</table>