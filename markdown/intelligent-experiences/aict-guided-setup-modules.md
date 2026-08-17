---
title: Guided setup areas
description: Area-by-area listing of the setup items in guided setup, with cross-references to the topic each item relates to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-guided-setup-modules.html
release: australia
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Guided setup, Configure, AI Control Tower, Enable AI experiences]
---

# Guided setup areas

Area-by-area listing of the setup items in guided setup, with cross-references to the topic each item relates to.

Guided setup groups setup items into the areas listed in this topic. The order of areas and items shown here matches the order in which guided setup displays them.

## Users and roles

Assign users to the groups that grant access to AI Control Tower.

|Setup area|Setup item|Description|
|----------|----------|-----------|
|Users and roles|Assign users to roles|Assign users to the AI Stewards, AI Product Owners, and AI Risk and Compliance Managers groups to grant them the corresponding permissions. For more information, see [Configure users and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-users-and-roles.md).|

## AI asset inventory

Bring ServiceNow and external AI assets into your inventory, and decide which assets participate in governance, monitoring, and value workflows.

|Setup area|Setup item|Description|
|----------|----------|-----------|
|AI asset inventory|Manage ServiceNow AI assets|Review AI systems, models, prompts, and datasets that AI Control Tower discovers automatically, and mark them as managed to bring them into governance, monitoring, and value workflows. For more information, see [Managing your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-ai-asset-inventory.md).|
|Discover external AI assets|Configure external connectors|Connect to cloud hyperscalers or SaaS applications to discover AI assets automatically and bring them into your inventory. For more information, see [Configuring Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-connectors.md).|
|Discover external AI assets|Set up traces|Connect to AWS, Microsoft Azure, or Google Cloud to collect trace data, discover AI agents running on those platforms, and generate evaluation and security metrics. For more information, see [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md).|
|Mark AI assets as Managed|Mark assets as Managed manually|Select assets from your inventory and mark them as managed to give them access to governance, value assessment, risk classification, monitoring, and security capabilities. For more information, see [Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-ai-managed-unmanaged.md).|
|Mark AI assets as Managed|Set rules to mark assets as Managed|Create or activate automation rules that mark discovered AI assets as managed automatically, based on conditions you define. For more information, see [Edit an automation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-automation-rules.md).|

## Value and cost configuration

Configure the templates and cost inputs used to calculate the value your AI assets deliver.

|Setup area|Setup item|Description|
|----------|----------|-----------|
|Value and cost configuration|Value templates|Select from existing value templates or create custom templates to define, calculate, and track the value your AI assets deliver. For more information, see .|
|Value and cost configuration|Cost framework|Configure cost and productivity inputs, such as hourly rates and AI costs by vendor, to calculate the net return on your AI investment. For more information, see [Configuring Cost in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-ai-configuring-aict-value-cost.md).|

## ServiceNow AI settings

Configure data sharing, deployment approval, and AI model provider settings that apply across your instance, not just AI Control Tower.

|Setup area|Setup item|Description|
|----------|----------|-----------|
|ServiceNow AI settings|Configure data control preferences|Set how your organization shares data with ServiceNow and manages data traffic during peak usage. For more information, see [Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md).|
|ServiceNow AI settings|Set builder controls|Require AI steward approval before AI assets deploy, and automate approval requests when new AI assets are added. For more information, see [Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md).|
|ServiceNow AI settings|Configure AI model providers|Choose which AI model providers are allowed on your instance and set fallback behavior for AI systems whose providers aren't on the allowed list. For more information, see [Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md).|

**Parent Topic:**[Guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-guided-setup.md)

