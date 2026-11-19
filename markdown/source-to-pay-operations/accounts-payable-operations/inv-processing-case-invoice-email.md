---
title: Configure Invoice Processing Case for Invoice Email flow
description: Configure the invoice processing case invoice email flow to process invoices received through email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/inv-processing-case-invoice-email.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Document Intelligence, Invoice processing case, Invoice email flow, Invoice Processing Case for Invoice email flow]
breadcrumb: [Configure Document Intelligence using ServiceNow Otto for Accounts Payable Operations \(APO\), Configure ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Invoice Processing Case for Invoice Email flow

Configure the invoice processing case invoice email flow to process invoices received through email.

## Before you begin

Role required: admin

Scope: Accounts Payable Operations integration with Document Intelligence.

Plugins required:

-   ServiceNow Otto in Document Intelligence
-   Account Payable Invoice Processing
-   ServiceNow Otto for Accounts Payable Operations \(APO\)
-   Document Intelligence for Accounts Payable Operations Content Pack

## Procedure

1.  Navigate to **All** &gt; **Flow designer** &gt; **Workflow Studio** &gt; **Flows**.

2.  Search for **Invoice Processing Case for Invoice email** flow.

3.  Select the \[Omitted image "more-actions.png"\] Alt text: more actions icon &gt; **Copy flow**.

    A copy of the **Invoice Processing Case for Invoice email** is created.

4.  Open the TRIGGER &gt; Inbound Email.

5.  Update the email conditions according to your business requirements.

    \[Omitted image "inv-proceesing-email.png"\] Alt text: Invoice processing case for invoice email

    **Note:** If you're upgrading Accounts Payable Operations from previous versions to version 12, then you must deactivate the existing **Invoice Processing Case for Invoice email** flow and make a fresh copy of the **Invoice Processing Case for Invoice email** flow to process invoices received through email.

6.  Select **Done**.

7.  Select **Activate**.

    The Invoice Processing Case for Invoice email flow is activated.


## Result

The invoice processing case invoice email flow is configured to process invoices received through email.

