---
title: Approval summarizer formatter
description: The approval summarizer formatter creates the summary at the bottom of an approval form.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approval summarizer formatter

The approval summarizer formatter creates the summary at the bottom of an approval form.

The approval summarizer displays different information depending on what is being approved, such as a change request or a service catalog request. Following are two examples.

![](../image/SummaryOfAChangeRequest.png "Summary of a change request")

![](../image/SummaryOfACatalogRequest.png "Summary of a catalog request")

The **Reject** button allows the approver to deny one or more requested items in a multi-item request, before approving the overall request. If a requested item is denied, the workflow for that item never starts. The approver can then choose to **Accept** the item.

**Note:** When the overall request is approved, you must ensure this **Reject** button is hidden. If this button is used after request approval, the requested item workflow is canceled, leaving the stage in an inconsistent state. Similarly, the **Accept** button on requested items should only appear before the overall request is approved or rejected.

-   **[Summarizers](../concept/c_Summarizers.md)**  
Approval summarizers are stored in the Macro \[sys\_ui\_macro\] table.

**Parent Topic:**[Classic approvals](r_Approvals.md)

**Related topics**  


[Using formatters](https://www.servicenow.com/docs/access?context=c_Formatters&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

