---
title: Reject an invoice manually
description: Review exceptions flagged for manual rejection and reject an invoice from the invoice case when AP specialist confirmation is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/reject-an-invoice-manually.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Create an invoice line manually, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Reject an invoice manually

Review exceptions flagged for manual rejection and reject an invoice from the invoice case when AP specialist confirmation is required.

## Before you begin

Role required: admin

The invoice must have at least one exception with **Rejection mode** set to **Manual**, and no exception with **Rejection mode** set to **Auto**.

## About this task

When exceptions flagged for manual rejection exist on an invoice, the system routes the invoice to an AP specialist for review. The invoice case displays a notification indicating that exceptions require manual rejection review. Use this procedure to review the exceptions and reject the invoice.

**Important:**

Manual rejection review is only triggered when no exception has **Rejection mode** set to **Auto**. If an auto rejection exception exists on the same invoice, the system rejects the invoice automatically and does not route it for manual review.

## Procedure

1.  Navigate to the invoice case that requires manual rejection review.

    The invoice case displays a notification that exceptions are flagged for manual rejection and require review.

2.  Review the exceptions listed on the invoice case.

    The **Rejection mode** field is visible on each exception record. Verify that the exceptions flagged for manual rejection are correct before proceeding.

3.  Select **Reject invoice**.

    A dialog prompts you to enter a rejection reason.

4.  Enter a rejection reason in the field provided.


## Result

After you confirm the rejection, the system performs the following actions:

-   Cancels the exception.
-   Cancels the invoice and closes the invoice processing case with the appropriate terminal state.
-   Populates the rejection reason and comments in the invoice audit history and activity stream.
-   Sends an email notification to the supplier with the rejection comments.

**Parent Topic:**[Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md)

