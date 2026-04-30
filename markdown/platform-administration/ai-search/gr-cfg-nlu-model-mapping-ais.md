---
title: AI Search Genius Result Configuration NLU Model Mapping form
description: The AI Search Genius Result Configuration NLU Model Mapping form contains information about relationships between Genius Result configurations and NLU models for AI Search. Use this form when linking Genius Result configurations to NLU models.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Genius Result Configuration NLU Model Mapping form

The AI Search Genius Result Configuration NLU Model Mapping form contains information about relationships between Genius Result configurations and NLU models for AI Search. Use this form when linking Genius Result configurations to NLU models.

For details on linking Genius Result configurations to NLU models, see [Link an NLU model and intents to a Genius Result configuration](../task/link-nlu-model-genius-result-ais.md).

|Field|Description|
|-----|-----------|
|Genius Result Configuration|The Genius Result configuration to link the NLU model to. This field is automatically set to the selected Genius Result configuration.|
|NLU Model|Existing NLU model to use for the Genius Result configuration's NLU trigger condition.|
|State|Current state of the selected NLU model. This field is automatically set.|
|Intents|List of intents from the NLU model that can trigger the Genius Result configuration when detected in the search query.|
|Order|Order of evaluation for the NLU model in the context of the Genius Result configuration.|
|Application|Application scope for the NLU model link. This field is automatically set.|

**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

