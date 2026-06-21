---
title: Approval summarizer formatter
description: The approval summarizer formatter creates the summary at the bottom of an approval form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/approval-summarizer.html
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Formatters, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Approval summarizer formatter

The approval summarizer formatter creates the summary at the bottom of an approval form.

The approval summarizer displays different information depending on what is being approved, such as a change request or a service catalog request. Following are two examples.

\[Omitted image "SummaryOfAChangeRequest.png"\] Alt text: Summary of a change request.

\[Omitted image "SummaryOfACatalogRequest.png"\] Alt text: Summary of a catalog request.

The **Reject** button allows the approver to deny one or more requested items in a multi-item request, before approving the overall request. If a requested item is denied, the workflow for that item never starts. The approver can then choose to **Accept** the item.

**Note:** When the overall request is approved, you must ensure this **Reject** button is hidden. If this button is used after request approval, the requested item workflow is canceled, leaving the stage in an inconsistent state. Similarly, the **Accept** button on requested items should only appear before the overall request is approved or rejected.

**Parent Topic:**[Formatters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_Formatters.md)

