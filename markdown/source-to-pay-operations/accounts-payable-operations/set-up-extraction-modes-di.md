---
title: Configure data extraction modes
description: Configure Document Intelligence extraction modes for invoice processing use cases to define how fields are extracted from invoice documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/set-up-extraction-modes-di.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Data extraction, APO, Accounts Payable Operations, AI automation, AP case]
breadcrumb: [Configure Document Intelligence using Now Assist for Accounts Payable Operations \(APO\), Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure data extraction modes

Configure Document Intelligence extraction modes for invoice processing use cases to define how fields are extracted from invoice documents.

## Before you begin

Role required: sn\_docintel.manager

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the workflow group, select &gt; **Finance and Supply Chain** &gt; **Invoice data extraction** to view the skills for the APO features.

3.  Select the settings \[Omitted image "icon-docintel-settings-gear.png"\] Alt text: docintel settings icon.

4.  Select the extraction mode for the use case**Accounts Payable Operations**.\[Omitted image "settings-na.png"\] Alt text: Extraction mode

5.  Adjust the DocIntel full automation mode.

    -   When Full automation mode is turned on, DocIntel automatically completes and submits the document task. The required values or fields in the invoice document are auto-filled or identified as missing in the document. If there are no fields defined as required for the document task, then DocIntel automatically completes and submits the document task.
    -   When you turn on the **Any required field is missing in the document**, the full automation mode is turned off and requires an agent review.
6.  Select **Save**.


