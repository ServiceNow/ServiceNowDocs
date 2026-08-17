---
title: Discovering and managing AI assets
description: Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-discovering-ai-assets.html
release: australia
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Discovering and managing AI assets

Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.

## Why discovery matters

Before you can govern, monitor, or measure the impact of AI, you need to know what AI assets exist in your organization. Many enterprises operate dozens or hundreds of AI systems across business units, with no single team holding a complete picture. Shadow AI, untracked models, and undocumented integrations create blind spots in governance and risk management. AI Control Tower addresses this by providing multiple discovery pathways that feed into a single AI asset inventory — a centralized record of every AI system, model, prompt, dataset, and MCP server across your enterprise.

## Managing your AI assets

You can view and manage AI assets across your entire portfolio or focus on a single asset.

The **Inventory** page gives you a complete picture of every AI system, model, prompt, dataset, and MCP server in your organization. From here, you set management status, filter by asset type or lifecycle stage, manually add assets that aren't reachable by automated methods, and respond to recommendations that flag assets needing attention. See [Managing your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-ai-asset-inventory.md).

The asset record page is where you investigate and act on a single asset. Open a record to review its governance posture, evaluation scores, lifecycle progress, and value contribution, and to initiate actions such as starting a lifecycle review, submitting a change request, or turning on evaluation. See [Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-managing-ai-assets.md).

## Discovering ServiceNow AI assets automatically

ServiceNow AI assets including skills, agents, and models running natively on your instance are discovered automatically. No manual configuration is required. As AI capabilities are activated on your instance, the discovery process detects and registers them in the AI asset inventory, giving your governance team visibility into every ServiceNow AI system from the moment it is deployed.

Automatic discovery eliminates the risk of ServiceNow AI systems operating outside the governance framework. Every skill, every AI agent built in AI Agent Studio, and every model connection is tracked and available for lifecycle management, risk assessment, and performance monitoring.

## Discovering external AI assets with Service Graph Connectors

Most enterprises run AI on more than one platform. Service Graph Connectors extend AI Control Tower's visibility beyond ServiceNow by discovering AI assets running on external platforms and synchronizing them into the inventory.

Each connector requires an AI connection — a configured credential and endpoint that allows AI Control Tower to communicate with the external platform. Once configured, the connector runs on a schedule to discover new assets, update existing records, and synchronize metadata. Some connectors also collect usage and execution data, enabling monitoring and value measurement for external AI alongside ServiceNow AI.

For organizations that operate AI across hyperscaler environments, AI Control Tower also supports hyperscaler connections for asset discovery and trace collection. These connections collect trace data from AWS, Azure, and GCP through a MID Server, without requiring SDK instrumentation in agent code.

