---
title: Discovering and managing AI assets
description: Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-discovering-ai-assets.html
release: australia
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Discovering and managing AI assets

Get a complete picture of every AI system in your organization by building and maintaining a comprehensive AI asset inventory.

## Why discovery matters

Before you can govern, monitor, or measure the impact of AI, you need to know what AI assets exist in your organization. Many enterprises operate dozens or hundreds of AI systems across business units, with no single team holding a complete picture. Shadow AI, untracked models, and undocumented integrations create blind spots in governance and risk management. AI Control Tower addresses this by providing multiple discovery pathways that feed into a single AI asset inventory — a centralized record of every AI system, model, prompt, dataset, and MCP server across your enterprise. See [Discovering AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-discovering-ai-assets.md).

## AI asset inventory

View and manage AI assets across your entire portfolio or focus on a single asset in the AI Control Tower inventory.

The **Inventory** page is designed to give you a complete picture of every AI asset in your organization. From the inventory, you can make assets managed or unmanaged, filter by asset type or lifecycle stage, manually add assets that aren't reachable by automated methods, and respond to recommendations for assets that need attention. See [Managing your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-ai-asset-inventory.md).

## AI asset records

The asset record is where you investigate and act on a single asset. In the asset record, you can review the asset's governance posture, evaluation scores, lifecycle progress, and value contribution. You can initiate asset-level actions such as starting a lifecycle review, submitting a change request, or turning on evaluation. See [Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-managing-ai-assets.md).

## Discovering unsanctioned AI use with Shadow AI

Connectors and manual entry only find AI systems your organization already knows to look for. Shadow AI detects AI use that never went through an official channel instead, such as an employee sending data to a public AI tool your organization hasn't sanctioned. It relies on multiple independent detection methods, including **Armis** and **Agent Client Collector** \(ACC\), to observe traffic and endpoint activity for signs of that use.

Because these detections represent AI systems your organization hasn't reviewed yet, Shadow AI keeps them in their own space rather than mixing them into the governed AI asset inventory. An AI steward reviews each detected service and decides how to respond, such as snoozing it for more time, blocking access, or confirming it's not actually an AI service. See [Detecting shadow AI in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-landing.md).

