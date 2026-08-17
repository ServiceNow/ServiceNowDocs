---
title: AI Control Tower playbooks
description: AI Control Tower ships with three active playbooks that drive the lifecycle and approval workflows for AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-playbooks-reference.html
release: australia
topic_type: reference
last_updated: "2026-04-28"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# AI Control Tower playbooks

AI Control Tower ships with three active playbooks that drive the lifecycle and approval workflows for AI assets.

Playbooks define the structured workflows that guide AI stewards and asset owners through asset onboarding, offboarding, and approval. The playbooks listed here are active by default and can't be edited from within AI Control Tower. To modify a playbook's logic or steps, open it in Workflow Studio by selecting the external link icon on the playbook record.

View and manage playbooks at **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Playbooks**.

## Playbooks

|Playbook|Description|
|--------|-----------|
|AI Asset Onboarding|Guides an AI asset through the onboarding lifecycle stages: Onboard, Assess, Build and test, and Deploy. Triggered when an asset is moved to managed and a lifecycle review is started. The playbook assigns tasks to AI stewards and asset owners for each phase and tracks completion before the asset moves to the Maintain phase.|
|AI Asset Offboarding|Guides an AI asset through the offboarding lifecycle stages: Assess, Pre-offboarding tasks, and Offboard. Triggered when an AI asset change request of type Offboarding reaches the In progress state. The playbook assigns tasks to the AI Stewards group and requires an approved assessment before the asset's inventory state and status update to Retired on completion.|
|Now Assist approval|Coordinates AI steward approval before a Now Assist AI asset is deployed. The playbook runs in three steps: Review asset, Evaluate asset, and Approve or reject. During the Evaluate asset step, AI stewards can create sub-approval tasks to gather input from other teams, such as Legal, Security, Data, or Privacy review. When approving or rejecting, the AI steward selects a Risk score and enters Close notes; these values become read-only after the step is marked complete. The playbook runs automatically when a new AI asset is added if AI steward approval is activated in Builder controls. See [Configure ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-ai-settings.md).|

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring.md)

