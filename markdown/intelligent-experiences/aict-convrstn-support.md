---
title: ServiceNow Otto in AI Control Tower
description: Ask questions about your AI portfolio in plain language and get answers drawn from your own AI Control Tower records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-convrstn-support.html
release: brazil
topic_type: concept
last_updated: "2026-09-09"
reading_time_minutes: 2
keywords: [generative AI, agentic AI, AI Control Tower, Otto premium chat, Conversational support, AICT Assistant]
breadcrumb: [Explore, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# ServiceNow Otto in AI Control Tower

Ask questions about your AI portfolio in plain language and get answers drawn from your own AI Control Tower records.

## How the conversational interface works

ServiceNow Otto is the conversational experience in AI Control Tower. It provides agentic orchestration on top of the premium chat in the ServiceNow AI Platform.

In AI Control Tower, the chat is delivered by an assistant named AICT Assistant, which is installed with the ServiceNow Otto for AI Control Tower application \(`com.sn_aict_genai`\). The chat window itself displays ServiceNow Otto, so the AICT Assistant name appears only where the underlying record is shown, such as in your AI asset inventory.

A dedicated assistant keeps the conversation scoped to AI Control Tower. Answers about your AI portfolio stay consistent because the other assistants configured on your instance don't take part in the conversation.

Answers are drawn from data retrieved from your instance at the time you ask. The assistant is configured to answer only from that retrieved data rather than from the general knowledge of the underlying model, so responses reflect the records in your own inventory and governance tables. When the assistant can't find an answer in your data, it tells you so rather than filling the gap.

## Use cases

The assistant answers questions that span your inventory, risk, compliance, security, and usage records. For example:

-   Find the AI systems that a particular business unit or business application owns, without constructing a query.
-   See how your AI models break down by provider, so you know where your model dependencies concentrate.
-   Identify AI systems with no recent usage, which are candidates for review or decommissioning.
-   Check inherent risk ratings across your portfolio to find assets that need attention first.
-   Review security findings such as threat results and privileged activity for a given asset.

Responses can include an inline widget alongside the text answer, so results that are clearer visually are presented that way.

## AICT Assistant in your AI asset inventory

AICT Assistant is the AI asset that represents the ServiceNow Otto conversational experience in AI Control Tower. Automatic discovery of ServiceNow AI assets registers the assistants on your instance, so your conversational experience is inventoried alongside the rest of your AI portfolio. See [Discovering ServiceNow AI assets automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/disc-discovering-servicenow-assets.md).

To locate the asset, search your inventory for AICT Assistant.

Bringing AICT Assistant under management applies the same governance to your conversational experience that you apply to the rest of your AI portfolio, including evaluation scoring, lifecycle stages, risk classification, and value tracking. Like other discovered ServiceNow AI assets, AICT Assistant arrives unmanaged. See [Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/disc-ai-managed-unmanaged.md) and [Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/disc-managing-ai-assets.md).

You can edit or customize the AICT Assistant in Assistant Designer. See [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/assistant-designer.md).

