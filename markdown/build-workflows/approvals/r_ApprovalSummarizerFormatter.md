---
title: Approval summarizer formatter
description: The approval summarizer formatter creates the summary at the bottom of an approval form.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Build workflows]
---

# Approval summarizer formatter

The approval summarizer formatter creates the summary at the bottom of an approval form.

The approval summarizer displays full information for the record used to request approval.

![The approval summarizer displays information from the original request directly in the approval request.](../image/SummaryOfAChangeRequest.png "Summary of a change request")

The **Reject** button allows the approver to deny one or more requested items in a multi-item request, before approving the overall request. If a requested item is denied, the workflow for that item never starts. The approver can then choose to **Accept** the item.

**Note:** When the overall request is approved, you must ensure this **Reject** button is hidden. If this button is used after request approval, the requested item workflow is canceled, leaving the stage in an inconsistent state. Similarly, the **Accept** button on requested items should only appear before the overall request is approved or rejected.

**Related topics**  


[bundle-platadm.c_Formatters]

