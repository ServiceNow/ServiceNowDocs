---
title: Resolve unverified sender source exception
description: Review an unverified sender source exception in APO and resolve it by adding the sender as a supplier contact or rejecting the invoice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/resolve-unverified-sender-exception.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Work on an invoice exception, Invoice exceptions, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Resolve unverified sender source exception

Review an unverified sender source exception in APO and resolve it by adding the sender as a supplier contact or rejecting the invoice.

## Before you begin

Role required: admin

An invoice with an unverified sender source exception must be assigned to you or your queue in APO.

## About this task

Use this procedure when an invoice is flagged with an unverified sender source exception. The exception indicates that the sender's email address or domain could not be verified against the supplier record or vendor contact list. You must review the exception details and take one of the available actions to resolve it.

The system evaluates the following conditions in order when an invoice email is received:

Condition A: Internal forwarding check.

The system first checks whether the email was forwarded by an internal employee.

-   If the sender's email domain matches the internal email domain, no exception is created. The system adds an audit log entry: *Success: Unverified Sender Source - Sender is found to be internal company employee.*
-   If the sender's email domain does not match the internal email domain, the system proceeds to evaluate Condition B.

Condition B: Known supplier, unknown contact.

The system evaluates this condition when the sender is not an internal employee. It applies when the supplier is successfully identified on the invoice \(via OCR or purchase order match\) but the sender's email address is not recognized.

-   The system checks whether all of the following are true:
    -   The supplier is identified as valid.
    -   The sender is not found in the vendor contact list.
    -   The sender's email domain matches the supplier's website domain or registered email domains in the primary supplier data or supplier contacts, OR the sender's email domain matches the email domain of other contacts in the vendor contact list.
-   If a domain match is found, the exception is created. The system adds an audit log entry: *Failed: Unverified Sender Source - Supplier identified and sender is found to be un-registered contact.*
-   If no domain match is found, the exception is created. The system adds an audit log entry: *Failed: Unverified Sender Source - Supplier identified but sender's email source is unknown.*

## Procedure

1.  Navigate to **Source-to-Pay Workspace** &gt; **All** &gt; **List** &gt; **Invoices**.

    locate the invoice with the unverified sender source exception.

2.  Select the invoice to open the exception record, then select the **Exception details** tab.

3.  Review the exception details and the audit log to understand why the exception was triggered.

    The audit log records one of the following outcomes:

    -   Failed: Exception check - Supplier identified and sender is found to be un-registered contact — the supplier is recognized but the sender is not in the vendor contact list, though the domain matches a known supplier domain.
    -   Failed: Exception check - Supplier identified but sender's email source is unknown — the supplier is recognized but the sender's email domain does not match any known supplier domain or contact.
4.  Select one of the following actions to resolve the exception:

    To add the sender as a new supplier contact and reprocess the invoice, select **Add contact to supplier**. For the steps to complete this action, see [Add a supplier contact from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-contact.md).

    **Note:**

    This option is available only if the Supplier Lifecycle Operations application is installed on your instance.

    To reject the invoice, select **Reject invoice**. A rejection dialog appears. Continue to the next step.\[Omitted image "unverified-sender.png"\] Alt text: Review an unverified sender source exception in APO


## Result

If you rejected the invoice, the system performs the following actions:

-   Adds the rejection reason to the exception record and invoice.
-   Cancels the invoice and the invoice processing \(IP\) case.

If you added the sender as a supplier contact, the invoice is reprocessed.

**Parent Topic:**[Work on an invoice exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-invoice-exception-case.md)

**Related topics**  


[Add a supplier contact from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-contact.md)

