---
title: External Registries
description: External Registries is the mechanism that lets an AI Steward make a managed AI agent discoverable to external systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/external-registries.html
release: australia
topic_type: concept
last_updated: "2026-07-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# External Registries

External Registries is the mechanism that lets an AI Steward make a managed AI agent discoverable to external systems.

When an AI agent is added to the inventory, AI Control Tower tracks whether it can be published to external registries. The publish-ability status appears in the External registries section of the AI asset detail record and can be changed at any time by an AI steward.

AI Control Tower no longer pushes agents to Microsoft. Instead, an AI steward marks an agent as publishable, which exposes it through a ServiceNow API. External systems such as Microsoft Agent 365 \(A365\) can then call this API at their own schedule \(example: a periodic daily job\) to discover and retrieve those agents.

Publishing an AI agent to an external registry makes it discoverable outside the AI Control Tower. Marking an agent as unpublishable removes it from consideration for external publication while keeping it active in the inventory. The agent continues to operate and is still managed by AI Control Tower regardless of its publish-ability status.

**Note:** Changing the publish-ability status of an AI agent does not affect its operational status or governance controls within AI Control Tower.

## Eligibility Criteria for Publishing

An Agentic AI asset must meet all four of the following criteria before the External Registries tab appears and the publish action is set to available:

|Criteria|Required value|
|--------|--------------|
|Governed|True|
|Lifecycle state|Deployed|
|Asset status|Approved|
|Agent model category|Agentic AI|
|ServiceNow table|AI agent|

## Publish-ability states

An AI agent can have one of the following publish-ability states:

-   Publishable- The AI agent is available for publication to external registries. AI Stewards can publish the agent and manage its external presence from AI Control Tower.
-   Unpublishable- The AI agent is not available for publication to external registries. AI stewards can restore publish-ability at any time by selecting Mark as publishable from the actions menu on the asset detail record.

**Note:** The Microsoft integration provides the following methods to publish an AI agent so that Microsoft can discover it:

-   An AI Steward can mark an AI agent as publishable or unpublishable directly from the AI asset record page.
-   An AI Steward can mark an AI agent as publishable or unpublishable in the corresponding Onboarding playbook. This option is available through the Publish to External Registries task of the Deploy activity. For more information on the Onboarding playbook, see [AI Control Tower playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-playbooks-reference.md).

If an AI agents meets all eligibility criteria, it is marked as publishable and returned by the discoverable APIs.

## External Registry Support

Currently, Microsoft Agent 365 is the only supported external registry in the UI. However, the API is open by design and any third-party system can call the endpoint to retrieve publishable agents.

## API Endpoints

Two API endpoints have been exposed for external systems:

-   List endpoint- Returns a list of all agents marked as publishable.
-   Detail endpoint- Returns detailed metadata for a specific agent, as required by Microsoft for display in Agent 365.

