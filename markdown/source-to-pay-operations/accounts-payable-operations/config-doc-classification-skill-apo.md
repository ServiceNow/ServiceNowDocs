---
title: Configure Accounts payable document classification skill
description: Configure the Document classification skill to automatically identify and categorize incoming documents by type before the invoice extraction process begins.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Configure Accounts payable document classification skill

Configure the Document classification skill to automatically identify and categorize incoming documents by type before the invoice extraction process begins.

## Before you begin

Role required: admin

Scope: Accounts Payable Operations integration with Document Intelligence.

Plugins required:

-   Now assist in Document Intelligence
-   Account Payable Invoice Processing
-   Now assist for Account Payable Operations
-   Document Intelligence for Accounts Payable Operations Content Pack

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist skills for Common Finance &amp; Supply Chain features** tab of the Now Assist Admin console.

2.  Select **Finance and Supply Chain** &gt; **Accounts Payable Operations** &gt; **Accounts payable document classification** to view the skills for the APO features.

3.  Select **Activate** the skill.

4.  Select **Save and continue**.

5.  In the **Review and activate** section, select **Activate**.

    The **Accounts payable document classification** use case is provided as out of the box within the skill. Make a copy of the following OOB flows in the flow designer and activate.

    -   [Invoice processing case for invoice email](inv-processing-case-invoice-email.md)
    -   [Process classification attachment using DI](process-classification-attachment-di.md)
    -   [Classification values on invoice staging](set-classification-values-on-invoice-stage.md)
    -       **Note:** The **Manual Classification on DI Error** scheduler runs every 30 minutes, checking for invoice cases where the DocIntel status is stuck in processing classification, and performs the following actions:

    -   Sets the DI status to Classification failed and the staging record status to Review required if all associated staging records are stuck in in-processing state
    -   Sets the DI status to Classification STP failed and the staging record status to Review required if some associated staging records are stuck in in-processing state
    The **Manual Classification on DI Error** scheduler is inactive by default. Activate the scheduler to pick invoice cases that are stuck in processing classification.

    The **Accounts payable document classification** is activated and the incoming email with attached documents are automatically categorized into invoices in the workspace.


