---
title: AI Control Tower playbooks
description: Drive the lifecycle and approval workflows for AI assets using playbooks in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-playbooks-reference.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Control Tower playbooks

Drive the lifecycle and approval workflows for AI assets using playbooks in AI Control Tower.

Playbooks define the structured workflows that guide AI stewards and asset owners through asset onboarding, offboarding, and approval. The playbooks are active by default and can't be edited from within AI Control Tower. To modify a playbook's logic or steps, open it in Workflow Studio by selecting the playbook.

**Important:**

The V1 AI asset onboarding playbook no longer receives updates. New customers use the V2 AI asset onboarding playbook. Existing customers can continue to use V1 or migrate to V2.

For more information about the deprecation process, see [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184).

## Playbooks

|Playbook|Description|
|--------|-----------|
|AI Asset Onboarding|Guides an AI asset through the onboarding lifecycle stages: Onboard, Assess, Build and test, and Deploy. Triggered when an asset is moved to managed and a lifecycle review is started. The playbook assigns tasks to AI stewards and asset owners for each phase and tracks completion before the asset moves to the Maintain phase.|
|AI Asset Offboarding|Guides an AI asset through the offboarding lifecycle stages: Assess, Pre-offboarding tasks, and Offboard. Triggered when an AI asset change request of type Offboarding reaches the In progress state. The playbook assigns tasks to the AI Stewards group and requires an approved assessment before the asset's inventory state and status update to Retired on completion.|
|Now Assist approval|Coordinates AI steward approval before a Now Assist AI asset is deployed. The playbook runs in three steps: Review asset, Evaluate asset, and Approve or reject. During the Evaluate asset step, AI stewards can create sub-approval tasks to gather input from other teams, such as Legal, Security, Data, or Privacy review. When approving or rejecting, the AI steward selects a Risk score and enters Close notes; these values become read-only after the step is marked complete. The playbook starts automatically when **Automatically trigger playbooks** is active on the **Builder controls** tab. Otherwise, an AI asset manager requests approval manually. See [Require AI steward approval for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-ai-steward-approval.md).|

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**  
Manage AI assets through structured lifecycle workflows using the updated playbooks that automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases.
-   **[Migrate to updated AI asset onboarding playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/migrate-new-playbook-govern.md)**  
Configure the new AI asset onboarding playbook to simplify AI asset management through structured lifecycle workflows. The migration also includes an opt-in to decide between moving to the new playbook or continuing in the existing playbook.

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring.md)

