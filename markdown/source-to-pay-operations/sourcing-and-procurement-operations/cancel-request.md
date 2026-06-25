---
title: Raise a cancel request
description: As a shopper, you can cancel an entire purchase request, purchase order, or individual line items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/cancel-request.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Purchase revision flows, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Raise a cancel request

As a shopper, you can cancel an entire purchase request, purchase order, or individual line items.

## Before you begin

Role required: sn\_spend\_psd.requestor or shopper

## Procedure

1.  Navigate to **ShoppingHub** &gt; **My purchases**.

    Alternatively, you can cancel a purchase from **Employee Center** &gt; **Purchase and Expense** &gt; **Purchase Requests** &gt; **Cancel a purchase**.

2.  Select a purchase requisition, purchase order, or purchase line.

3.  Select **Cancel this purchase** from the **Edit** menu or the **More options** menu.

    \[Omitted image "spo-cancel-purchase-from-pr.png"\] Alt text: Canceling a purchase from the purchase requisition.

    You can also select the **More options** icon on the requisition line and select **Cancel this purchase** to cancel a purchase.

    \[Omitted image "spo-cancel-purchase-from-pr-more-options.png"\] Alt text: Canceling a purchase from the More options menu of a purchase line.

    You can also cancel a purchase requisition line using the **Remove** button in the **Edit a purchase** page. It will internally create a new procurement case for the buyer to confirm or reject.

4.  Specify a reason for the cancellation.

    \[Omitted image "spo-cancel-a-purchase-form.png"\] Alt text: Specifying a reason for canceling this purchase.

5.  Select **Submit request**.


## Result

The step creates a procurement case with the details of the product for cancellation. Associated request lines and tasks are created using this information.

## What to do next

-   Shoppers can review and edit the request details from **ShoppingHub** &gt; **My requests** or **My requests** from the footer.
-   Buyers can review, edit, and process your request details from **Procurement Case Management** &gt; **Source-to-Pay Workspace** &gt; **Procurement Cases**, if required.

**Parent Topic:**[Purchase revision flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-revision-flows.md)

**Related topics**  


[Purchase revision flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-revision-flows.md)

[Process Automation Designer flows for playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/process-automation-designer-flows-psm.md)

