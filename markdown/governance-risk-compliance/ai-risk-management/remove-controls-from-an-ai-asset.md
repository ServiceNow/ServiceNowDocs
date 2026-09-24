---
title: Remove controls from an AI asset
description: Remove associated controls from an AI asset to keep the inventory accurate and up to date. This step is essential to retire outdated or irrelevant controls without deleting their records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/remove-controls-from-an-ai-asset.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [remove controls, disassociate controls, AI asset]
breadcrumb: [Manage controls, Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Remove controls from an AI asset

Remove associated controls from an AI asset to keep the inventory accurate and up to date. This step is essential to retire outdated or irrelevant controls without deleting their records.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst

## About this task

Removing a control disassociates it from the AI asset without deleting the underlying control record. The control remains in the inventory and can be re-added to the same or other AI assets later. Use Remove when a control is no longer applicable to an asset but the record itself should be preserved. To permanently delete control records, see [Delete controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/delete-controls-from-an-ai-asset.md).

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list \[Omitted image "ListsIcon.jpg"\] Alt text: icon.

3.  Navigate to the **AI asset inventory** and open the AI asset record.

4.  Navigate to **Applies to** &gt; **Controls**.

5.  Choose the control that you want to remove and select **Remove**.

    The **Remove** button appears only when an AI analyst is assigned to the AI asset record.

6.  Select **Remove all**.

    The selected controls for this AI asset are retired. This action doesn't delete the control records.


## Result

The selected controls are disassociated from this AI asset and their state changes to retired. The underlying control records remain in the inventory and can be re-added to this or other AI assets later.

## What to do next

To permanently remove control records from the system, see [Delete controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/delete-controls-from-an-ai-asset.md). To add controls back to this or another AI asset, see [Add controls from control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/add-controls-from-control-objective-airc.md).

**Parent Topic:**[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

**Related topics**  


[Add controls from control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/add-controls-from-control-objective-airc.md)

[Delete controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/delete-controls-from-an-ai-asset.md)

[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

