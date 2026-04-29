---
title: Submit a quote for advanced approval
description: Submit a quote for advanced approval to route it to required approvers before sharing it with a customer.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Quote Management, Configure, price, quote apps, Use, Sales and Order Management]
---

# Submit a quote for advanced approval

Submit a quote for advanced approval to route it to required approvers before sharing it with a customer.

## Before you begin

Advanced Approval Management must be installed to submit a quote for advanced approval.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer

## About this task

When you submit a quote for advanced approval, the system routes it to the required approvers based on configured approval rules and sequencing. You can also add ad-hoc approvers to the approval request when additional review is needed outside of the configured workflow.

If your administrator has configured reminder schedules, approvers receive automated notifications when their approval steps are pending. If an approval step is escalated, the step card displays the escalated approver so that all parties know who is responsible for the next action. Your administrator configures reminder and escalation settings.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List Icon.

3.  Navigate to **Quotes** &gt; **All**.

4.  Select the quote that you want to submit for approval.

5.  Select **Submit for approval**.

6.  In the Preview and request dialog, review the required approvals and their sequence.

7.  In **Message to approvers** field, enter comments for the approvers.

8.  Select **Request Approval**.


## Result

The quote is submitted for approval and enters the In Review state. Approval requests are generated based on configured approval rules and sequencing.

**Parent Topic:**[Using Quote Management](../concept/quote-mgmt-using.md)

