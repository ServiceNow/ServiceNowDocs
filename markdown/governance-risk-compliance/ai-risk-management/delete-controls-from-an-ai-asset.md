---
title: Delete controls from an AI asset
description: Delete controls from an AI asset to remove them permanently from the control table. This task confirms outdated or unnecessary controls are deleted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/delete-controls-from-an-ai-asset.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [delete controls, permanent control deletion, AI asset]
breadcrumb: [Manage controls, Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Delete controls from an AI asset

Delete controls from an AI asset to remove them permanently from the control table. This task confirms outdated or unnecessary controls are deleted.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

## About this task

Deleting a control permanently removes the control record from the system. This action cannot be undone. Use Delete only when the control record itself is outdated, duplicated, or should no longer exist in the inventory for any AI asset. If you want to disassociate a control from a specific AI asset while keeping the record available for future use, use Remove instead. For more information, see [Remove controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/remove-controls-from-an-ai-asset.md).

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list \[Omitted image "ListsIcon.jpg"\] Alt text: icon.

3.  Navigate to the **AI asset inventory** and open the AI asset record.

4.  Navigate to **Applies to** &gt; **Controls**.

5.  Choose the control that you want to delete and select **Delete**.

    The **Delete** button appears only when you have the required role assigned to perform this task.

6.  Select **Delete all**.

    The control records are deleted completely.


## Result

The selected control records are permanently deleted and can no longer be associated with any AI asset. This action cannot be undone.

## What to do next

To add new controls to the AI asset from available control objectives, see [Add controls from control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/add-controls-from-control-objective-airc.md). To disassociate controls without deleting them, see [Remove controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/remove-controls-from-an-ai-asset.md).

**Parent Topic:**[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

**Related topics**  


[Remove controls from an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/remove-controls-from-an-ai-asset.md)

[Add controls from control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/add-controls-from-control-objective-airc.md)

[Manage controls using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/manage-controls-in-airc.md)

