---
title: Discovering and managing AI assets
description: Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-discovering-ai-assets.html
release: australia
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use]
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Discovering and managing AI assets

Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.

## Why discovery matters

Before you can govern, monitor, or measure the impact of AI, you need to know what AI assets exist in your organization. Many enterprises operate dozens or hundreds of AI systems across business units, with no single team holding a complete picture. Shadow AI, untracked models, and undocumented integrations create blind spots in governance and risk management. AI Control Tower addresses this by providing multiple discovery pathways that feed into a single AI asset inventory — a centralized record of every AI system, model, prompt, dataset, and MCP server across your enterprise. See [Discovering AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/disc-discovering-ai-assets.md).

## AI asset inventory

View and manage AI assets across your entire portfolio or focus on a single asset in the AI Control Tower inventory.

The **Inventory** page is designed to give you a complete picture of every AI asset in your organization. From the inventory, you can make assets managed or unmanaged, filter by asset type or lifecycle stage, manually add assets that aren't reachable by automated methods, and respond to recommendations for assets that need attention. See [Managing your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/disc-ai-asset-inventory.md).

## AI asset records

The asset record is where you investigate and act on a single asset. In the asset record, you can review the asset's governance posture, evaluation scores, lifecycle progress, and value contribution. You can initiate asset-level actions such as starting a lifecycle review, submitting a change request, or turning on evaluation. See [Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/disc-managing-ai-assets.md).

## Connecting external AI through AI Gateway

AI Gateway manages MCP \(Model Context Protocol\) server connections, providing a governed pathway for external AI tools to interact with your ServiceNow environment. Where Service Graph Connectors focus on discovering what AI exists externally, AI Gateway focuses on governing how external AI tools connect to and operate within your platform.

When an MCP server is added through AI Agent Studio, AI Gateway tracks the connection, monitors transaction volumes and success rates, and enforces approval workflows if MCP server approval controls are active. AI stewards can review MCP server records, pause and resume transactions, and manage global MCP clients from the AI Gateway settings page.

AI Gateway provides a comprehensive view of all connected MCP servers, showing name, total transactions, and success rate. Total transactions represent all tool calls \(MCP method equal to "tools/call"\), and the success rate reflects the proportion of those calls returning a successful HTTP status.

