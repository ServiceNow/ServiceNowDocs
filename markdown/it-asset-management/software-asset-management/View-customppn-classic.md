---
title: View publisher part number \(PPN\) suggestions in Software Asset Management classic
description: View content service suggestions for your custom PPNs and DMAPS in the Software Asset Management classic application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# View publisher part number \(PPN\) suggestions in Software Asset Management classic

View content service suggestions for your custom PPNs and DMAPS in the Software Asset Management classic application.

## Before you begin

PPN suggestions are available only if a corresponding match is found for your custom PPN in the Content Service. The PPN suggestion records are stored in the Part number suggestions \[samp\_sw\_part\_number\_suggestion\] table.

Role required: sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Part number suggestions**.

2.  Open a suggestion record to view the Part number suggestion page.

    You can view the custom PPN details in the top part of the Part number suggestion page. The second half of the page contains the suggested part number details. All the entitlements where the custom PPN is used appear in the **Impacted entitlements** tab. All the software models where the custom DMAP is used appear in the **Impacted software models** tab. If no impacted software models exist, then this tab doesn't appear.

3.  Select **Accept** or **Reject**.

    -   **Accept**: The Content Service PPN and DMAP replace the custom PPN and DMAP. In the impacted entitlement, the content service PPN is replaced. Similarly, the content service DMAP is replaced on the software model.
    -   **Reject**: The status of this record changes to rejected and you continue to use the custom PPN.

**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

