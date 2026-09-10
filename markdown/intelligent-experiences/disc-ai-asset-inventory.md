---
title: Managing your AI asset inventory
description: Track every AI system, model, prompt, and dataset across your enterprise and control which assets participate in governance, monitoring, and risk workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-ai-asset-inventory.html
release: zurich
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managing your AI asset inventory

Track every AI system, model, prompt, and dataset across your enterprise and control which assets participate in governance, monitoring, and risk workflows.

## Key benefits

The AI asset inventory is the central record of AI assets in your organization. Assets that AI Control Tower discovers or identifies through traces appears here, organized by asset type.

-   Get a complete picture of every AI asset across your organization, including assets discovered automatically and those added manually or through connectors.
-   Control which assets participate in governance, monitoring, and risk workflows by setting management status directly from the inventory list.
-   Filter and refine the asset list by type, risk classification, lifecycle state, asset status, and management status to focus on what needs attention.
-   Add assets manually when a connector or trace can't reach them. See [Creating AI assets manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-ai-assets-newexperience.md).

For the ways AI Control Tower adds assets to your inventory automatically, see [Discovering AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-discovering-ai-assets.md).

\[Omitted image "disc-inventory.png"\] Alt text: Example AI asset inventory showing a list of AI assets showing asset types, asset states, asset status, management status, and evaluation status.

## AI assets list columns

|Column|Description|
|------|-----------|
|Name|The name of the AI asset as registered in AI Control Tower.|
|Asset type|The category of the AI asset, such as AI dataset, AI prompt, AI model,MCP server, or AI system.|
|State|The operational state of an AI asset.|
|Status|The governance status of the asset within its current phase.|
|Managed status|Indicates whether the asset is actively governed. Displays as true or false.|
|Domain|Domain the asset belongs to.|
|Managed by|The team or individual responsible for governing the asset.|
|Risk classification|The assessed risk level of an AI asset.|
|Updated|The date and time the asset record was last modified.|

## Required roles

The AI steward \[sn\_ai\_governance.ai\_steward\] or AI system owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role is required to access the AI asset inventory.

## Accessing the AI asset inventory

Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Assets**.

## AI systems

An AI system is a deployed AI application or capability that your organization uses to perform work. Examples include Now Assist skills, AI agents built in AI Agent Studio, and AI-powered applications running on external platforms. AI systems are the primary unit of governance in AI Control Tower, and the assets you classify for risk, assign stewards to, monitor for performance, and measure for value.

In the Inventory, AI systems are identified by asset type: Agentic AI, Generative AI, or Classic AI. Select the **AI systems** tab to filter to these three types together.

-   Filter to AI systems only to focus on the assets central to your governance program, regardless of provider.
-   Select an AI system record to review lifecycle details, risk classification, monitoring data, and value metrics in one place.
-   Designate AI systems as managed to bring them into governance workflows, or initiate a steward review to transition an unmanaged system automatically.

## AI models

An AI model is a machine learning model or large language model \(LLM\) that powers one or more AI systems. Tracking models in the inventory gives you visibility into which models are in use across your organization, which vendors supply them, and whether they are approved for their current deployment context.

-   Identify which models are active across your organization, including models imported from external providers such as OpenAI, Mistral AI, and Google.
-   Review provider, vendor, and lifecycle state for each model to confirm models are from approved sources and are current.
-   Spot models that may need review as vendors release new versions or as vendor relationships change.

## AI datasets

A dataset is a collection of data used for training, fine-tuning, or evaluating an AI model. Tracking datasets in the inventory supports data lineage, compliance documentation, and risk assessment for AI systems that depend on specific training data.

-   Track training, fine-tuning, and evaluation datasets alongside the models they support to maintain data lineage across your AI portfolio.
-   Review provider, asset state, and management status for each dataset to identify datasets that may affect risk classification for dependent AI systems.
-   Support compliance documentation by keeping a complete record of the data your AI models were built on.

## AI prompts

A prompt is a system prompt or prompt template that shapes the behavior of an AI system. Prompts define the instructions, context, and constraints an AI model operates under, making them a key governance asset for organizations that require AI behavior aligns with policy and acceptable use standards.

-   See all system prompts and templates in use across your organization's AI systems in one place.
-   Identify prompts that may need policy review or update as acceptable use standards evolve.
-   Understand the reach of any prompt change before making it by tracking which AI systems and models each prompt supports.

## Reviewing duplicate AI assets

AI asset deduplication can detect assets in your inventory that perform the same function, such as when two teams independently build similar AI agents to solve the same problem. AI Control Tower surfaces these likely duplicates as a group for an AI steward to review. The AI steward can then confirm the group as true duplicates or dismiss it, before changes are made to relevant asset records. For more information, see [Duplicate AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/review-duplicates.md).

## Managing the status of AI assets

Control whether an AI asset participates in governance workflows by setting its management status. Managed assets are included in lifecycle management, governance, risk classification, value assessment, security, and privacy capabilities. Unmanaged assets are tracked in the inventory but excluded from those workflows. For more information, see [Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-managed-unmanaged.md).

## Managing AI assets in bulk

Classify large numbers of AI assets automatically instead of moving them to managed one at a time by creating automation rules. A rule matches assets against conditions you define, such as asset type or usage patterns, and marks every matching asset as managed at each scheduled run. For more information, see [Managing AI assets in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-bulk-managing-assets.md).

## Managing evaluations

Detect quality and safety regressions in your managed AI assets by enabling evaluation. Evaluation scoring assesses AI interactions against configurable quality and safety metrics and surfaces trends so you can investigate regressions before they affect users. Disable evaluation when an asset no longer needs active scoring; historical scores are retained either way. For more information, see [Evaluating AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-evaluating-ai-assets.md).

## Deactivating managed AI agents

Deactivate a managed AI agent directly from its asset record using AI agent containment with kill switch protocol. For more information, see [Deactivate a managed AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-contain-managed-asset.md).

