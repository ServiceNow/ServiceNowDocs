---
title: Builder controls
description: Builder controls in AI Control Tower enable you to govern AI assets and workflows by requiring human approval before an asset is deployed or a playbook is triggered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/builder-controls.html
release: australia
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Configure ServiceNow AI settings, Configure, AI Control Tower, Enable AI experiences]
---

# Builder controls

Builder controls in AI Control Tower enable you to govern AI assets and workflows by requiring human approval before an asset is deployed or a playbook is triggered.

You can access Builder controls from the **Settings** page in AI Control Tower by selecting the **Builder controls** tab. Builder controls contain two governance settings:

-   AI Steward approval for AI assets
-   Automatically trigger playbooks

## AI Steward approval for AI assets

When you activate AI Steward approval, an AI Steward must approve an AI asset before it can be deployed. You can activate approval independently for each asset type.

The following asset types support AI Steward approval:

|Asset type|Status|Description|
|----------|------|-----------|
|AI systems|Inactive|Requires AI Steward approval before an AI system can be deployed.|
|Model Context Protocol \(MCP\) servers|Inactive|Requires AI Steward approval before an MCP server is made available.|
|AI models|Inactive|Requires AI Steward approval before an AI model can be used by AI systems.|

Each asset type has an independent status of Active or Inactive. When the status is Inactive, AI Steward approval is not enforced for that asset type.

**Note:** Activating AI Steward approval for one asset type does not affect the approval requirement for other asset types.

## Automatically trigger playbooks

The **Automatically trigger playbooks** setting controls whether an approval request is triggered automatically when an AI asset is added. When active, an approval request is sent automatically whenever an AI asset is added. When inactive, the asset manager initiates the request manually.

**Note:** If you don't activate **Automatically trigger playbooks**, asset managers must initiate approval requests manually from the asset record.

**Parent Topic:**[Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md)

