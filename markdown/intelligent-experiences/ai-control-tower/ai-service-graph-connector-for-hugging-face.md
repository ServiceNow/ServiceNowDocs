---
title: AI Service Graph Connector for Hugging Face
description: Use the  AI Service Graph Connector for Hugging Face to create AI connections to discover and import AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Hugging Face

Use the  AI Service Graph Connector for Hugging Face to create AI connections to discover and import AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Hugging Face app.

## Supported ServiceNow versions

-   Australia
-   Zurich

## User role

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from Hugging Face

-   Hugging Face account
-   Generate API Tokens

## Discovery scope

The HuggingFace connector discovers AI components from HuggingFace Spaces by analyzing Python files using pattern matching. The discovery process identifies:

-   AI agents/systems: Applications and agent implementations
-   AI models: Language models, embeddings, and other ML models
-   Tools: Function definitions and tool implementations
-   AI Prompts: Prompt templates and configurations

**Note:** The connector performs incremental discovery, only processing spaces that have been modified since it's last successful import.

