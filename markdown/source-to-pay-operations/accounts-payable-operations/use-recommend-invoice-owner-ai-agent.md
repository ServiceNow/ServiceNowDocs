---
title: Use Recommend invoice owner AI agent
description: Use the Recommend invoice owner AI agent to detect business owners for Non-PO invoices and Non-PO credit memos that lack an owner. The AI agent analyzes historically processed invoices to recommend the most likely business owner, which an accounts payable specialist can review, approve, or override.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-11-11"
reading_time_minutes: 1
keywords: [AI agent, Now Assist]
breadcrumb: [Recommend invoice owner AI agent, Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Use Recommend invoice owner AI agent

Use the Recommend invoice owner AI agent to detect business owners for Non-PO invoices and Non-PO credit memos that lack an owner. The AI agent analyzes historically processed invoices to recommend the most likely business owner, which an accounts payable specialist can review, approve, or override.

## Before you begin

Role required: Accounts Payable specialist \(sn\_ap\_apm.accounts\_payable\_specialist\)

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon ![](../../supplier-lifecycle-operations/image/cases-list-icon.png).

3.  Select **My work** &gt; **Invoice exceptions**.

4.  From the **Number** column, select the link for the 'Missing or invalid business owner' exception with the status **Review needed**.

    The missing or invalid business owner exception opens. A message that Now Assist has a resolution plan to solve the exception displays.

5.  Select **View plan**.![View resolution plan](../image/apo-view-resolution-plan.png)

    The AI agent summarizes the exception and provides a resolution plan. For more details on the resolution plan, see [Resolution plan scenarios](../reference/resolution-plan-scenarios.md).

6.  Review and confirm the resolution plan.![Confirm recommendation](../image/apo-confirm-resolution-plan.png)

    In this scenario, a business owner is assigned. ![Review and confirm the resolution plan](../image/apo-resolution-plan.png)


## Result

When a business owner is found, the AI agent updates the **Business owner** field on the invoice based on the closest matching invoice, updates the activity, and changes the exception status to **Review complete**.

If no business owner is found, the AI agent suggests creating a task.

**Parent Topic:**[Recommend invoice owner AI agent](../concept/recommend-invoice-owner-ai-agent.md)

**Related topics**  


[Configuring invoice owner prediction settings](../concept/configuring-bo-prediction-settings.md)

[Resolution plan scenarios](../reference/resolution-plan-scenarios.md)

