---
title: Configuring ServiceNow AI settings
description: Decide what AI data your instance shares with ServiceNow, which AI assets need AI steward approval before deployment, and which AI model providers your AI systems can use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configuring-servicenow-ai-settings.html
release: australia
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring ServiceNow AI settings

Decide what AI data your instance shares with ServiceNow, which AI assets need AI steward approval before deployment, and which AI model providers your AI systems can use.

ServiceNow AI settings apply across your instance and affect AI features throughout it, not only AI Control Tower. Review each setting against your organization's data governance and AI governance policies before you change it.

## Data controls

Data controls determine whether your instance contributes data that ServiceNow uses to improve its AI models, and whether ServiceNow Otto traffic can move to Microsoft Azure datacenters during traffic spikes. For more information, see [Configuring data controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-data-controls.md).

## Builder controls

Builder controls keep a human approval step between building an AI asset and deploying it. You decide which asset types need AI steward approval and whether approval requests start automatically. For more information, see [Configuring builder controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-builder-controls.md).

## AI model providers

AI model provider settings limit your AI systems to the providers your organization approves, determine where AI requests are processed, and determine what happens to AI systems that the approved providers don't support. Eligible instances can also enroll in the Model Preview Program here. For more information, see [Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md).

## Who can change these settings

Users with the AI steward \[sn\_ai\_governance.ai\_steward\] or admin role can view and change ServiceNow AI settings.

## Settings in a multi-instance environment

When multi-instance management is configured, the data sharing and data overflow processing preferences synchronize from the production \(manager\) instance to its sub-prod \(managed\) instances. On a sub-prod instance, those two settings are read-only, so change them on the production instance. For more information, see [Multi-instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-multi-instance.md).

-   **[Configuring data controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-data-controls.md)**  
Choose whether your instance contributes data that ServiceNow uses to improve its AI products, and whether ServiceNow Otto traffic can move to Microsoft Azure datacenters during traffic spikes.
-   **[Configuring builder controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-builder-controls.md)**  
Keep a human review between building an AI asset and deploying it by requiring AI steward approval for each asset type and triggering approval requests automatically.
-   **[Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md)**  
Limit your AI systems to the model providers your organization approves, control where AI requests are processed, and see how each change affects the AI systems on your instance before you save it.

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring.md)

