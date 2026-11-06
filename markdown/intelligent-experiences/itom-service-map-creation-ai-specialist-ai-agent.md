---
title: Service map AI agent
description: This AI agent runs automatically on a schedule and creates service maps from ML-based and tag-based candidates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/itom-service-map-creation-ai-specialist-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 3
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Service map AI agent

This AI agent runs automatically on a schedule and creates service maps from ML-based and tag-based candidates.

## Workflow

After you activate the agent from the Service Mapping home page, the agent runs automatically every 15 minutes. No user input is required for each candidate. On each run, the agent does the following:

1.  Finds the machine learning \(ML\) candidates and tag-based candidates that it hasn't processed in the last 90 days.
2.  Analyzes each candidate to determine whether it represents a business service.
3.  Creates a service map for each candidate that represents a business service. The service maps are non-operational by default so that an administrator can review them before activation.
4.  Records the outcome for each candidate. To see each run, open **AI Activity** in the Service Mapping list navigation.

## Retries for failed candidates

-   If the platform returns a temporary error, such as reaching the limit of concurrent AI agent plans, the candidate is processed at the next run.
-   If an invocation fails for any other reason, the candidate isn't retried automatically.

## Processing limit

By default, the agent can process 100 candidates for each candidate type. When the agent reaches the limit for a candidate type, it stops processing that candidate type and its status is set to **Paused**. The agent stays stopped until you raise the limit.

To raise the limit and reactivate the agent, first configure the following properties:

1.  For ML-based candidates: **sn\_sm\_gen\_ai.agent\_invocation\_limit.ServiceMapCreationAISpecialist**
2.  For tag-based candidates: **sn\_sm\_gen\_ai.agent\_invocation\_limit.TagBasedServiceMapCreationAISpecialist**

You can change the value based on your available AI resources. After raising the limit, reactivate the agent in the Service Mapping workspace.

**Note:** Raising the limit increases AI resource consumption, because the agent processes more candidates.

## AI agent configuration

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts for ML-based candidates**

create\_service\_topology

Get Candidate Running Processes

Get ML Candidate Full Data

Save Candidate Analysis

save\_run\_record

-   **Scripts for tag-based candidates**

create\_service\_topology

Get Tag Candidate Full Data

Get Tag Candidate Running Processes

Save Candidate Analysis

save\_run\_record


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

service\_mapping\_ai\_user, cmdb\_read, itom\_admin, snc\_internal, snc\_required\_script\_writer\_permission, sn\_bm\_client.benchmark\_data\_viewer, sn\_itom\_license.reader

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Operations Management at [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-ai-agents-overview.md)

