---
title: Copy and configure Invoice Processing Case for Invoice email flow
description: Configure the invoice processing case invoice email flow to process invoices received through email.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Configure Accounts payable document classification skill, Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Copy and configure Invoice Processing Case for Invoice email flow

Configure the invoice processing case invoice email flow to process invoices received through email.

## Before you begin

Role required: admin

Scope: Accounts Payable Operations integration with Document Intelligence.

Plugins required:

-   Now assist in Document Intelligence
-   Account Payable Invoice Processing
-   Now assist for Account Payable Operations
-   Document Intelligence for Accounts Payable Operations Content Pack

## Procedure

1.  Navigate to **All** &gt; **Flow designer** &gt; **Workflow Studio** &gt; **Flows**.

2.  Search for **Invoice Processing Case for Invoice email** flow.

3.  Select the ![more actions](../image/more-actions.png) icon &gt; **Copy flow**.

    A copy of the **Invoice Processing Case for Invoice email** is created.

4.  Open the TRIGGER &gt; Inbound Email.

5.  Update the email conditions according to your business requirements.

    ![Invoice processing case for invoice email](../image/inv-proceesing-email.png)

    **Note:** If you're upgrading Accounts Payable Operations from previous versions to version 12, then you must deactivate the existing **Invoice Processing Case for Invoice email** flow and make a fresh copy of the **Invoice Processing Case for Invoice email** flow to process invoices received through email.

6.  Select **Done**.

7.  Select **Activate**.

    The Invoice Processing Case for Invoice email flow is activated.


