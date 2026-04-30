---
title: View normalization suggestions in workspace
description: View normalization suggestion records in the Software Asset Workspace that are created for discovery models. You can accept or reject these suggestions.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License operations view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View normalization suggestions in workspace

View normalization suggestion records in the Software Asset Workspace that are created for discovery models. You can accept or reject these suggestions.

## Before you begin

Role required:

-   sam\_admin: accepts or rejects the normalization suggestions.
-   sam\_user: views normalization suggestions.

The normalization suggestion records are stored in the Normalization Suggestions \[samp\_normalization\_suggestions\] table.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select Normalization Suggestions in the Discovery list view

3.  Select a normalization suggestion record to view its details.

    For a detailed description of the normalization suggestion fields, see [Normalization suggestions for discovery models](../concept/normalization-suggestions.md).

4.  Select **Accept** to update the discovery model with the correct values or click **Reject** to retain the manually normalized values.

    **Note:** Only the sam\_admin role can accept or reject the normalization suggestions. For details on accepting or rejecting suggestions, see [Normalization suggestions for discovery models](../concept/normalization-suggestions.md).


