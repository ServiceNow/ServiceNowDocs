---
title: Catalog item request approaches
description: Catalog items can be requested conversationally, depending on how your admin has configured Virtual Agent and which approach is in use. The available approaches help you select the appropriate method for your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-catalog/catalog-agent.html
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 2
breadcrumb: [Conversational catalog item requests, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog item request approaches

Catalog items can be requested conversationally, depending on how your admin has configured Virtual Agent and which approach is in use. The available approaches help you select the appropriate method for your environment.

Four approaches are available to submit a catalog item request through Virtual Agent. Two approaches are current and actively supported; two are legacy paths that remain available for existing deployments.

## Catalog agent

The Catalog Agent uses AI-native conversation through ServiceNow Otto to guide requesters through a natural-language conversation, collecting answers step by step instead of presenting all fields at once.

When a catalog item is supported by the Catalog Agent, the request flows through the Catalog Agent. Where the Catalog Agent does not support an item, the request goes back to the LLM topic block if the conversation is supported. If the item is not supported conversationally at all, it opens in interactive view as a form.

## LLM topic block

The LLM topic block is the pre-existing conversational approach powered by Virtual Agent and generative AI. It uses reusable topic blocks to collect catalog item variables through a guided conversation.

The LLM topic block also serves as the secondary step for catalog items that the Catalog Agent does not support. The conversational flow — search, pre-summary card, questions, summary card — is preserved in both approaches.

For the conditions that determine whether a catalog item is conversational in the LLM topic block, see [Request catalog item through Now LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-catalog/request-topic-blocks-va-llm.md).

When a requester submits a catalog item request through Virtual Agent on NextWave, the request follows this sequence:

1.  Catalog Agent — If the catalog item is supported by Catalog Agent, the request is handled conversationally through Catalog Agent.
2.  LLM topic block — If the item is not yet supported by Catalog Agent, the request falls back to the LLM topic block, which handles it conversationally using the existing topic block flow.
3.  Interactive View \(form\) — If the item is not supported conversationally by either mechanism, it opens as a standard web form in Interactive View.

The conversational flow is largely consistent between Catalog Agent and the LLM topic block. Both paths present a pre-summary card, collect answers to catalog item questions, and display a summary card before submission. The underlying orchestration differs, but the requester experience is similar.

## NLU topic block

The NLU topic block is an existing approach that configured conversational catalog requests before the introduction of the LLM topic block. It remains available for existing deployments.

**Note:** For new conversational catalog configurations, use of Catalog agent or the LLM topic block is preferred.

## Form — Interactive View

When a catalog item can't be rendered conversationally — because it's not supported by the Catalog Agent or the LLM topic block — Virtual Agent opens the item as a standard web form in interactive view. This is the fallback for non-conversational items.

In NextWave, non-conversational items open in Interactive View.

## Choosing an approach

For most organizations that have not enabled conversational catalog requests, use the Catalog Agent. For organizations already running the LLM topic block, no migration is required — the LLM topic block remains supported, and Catalog Agent handles items incrementally as coverage expands.

**Parent Topic:**[Conversational catalog item requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-catalog/explore.md)

