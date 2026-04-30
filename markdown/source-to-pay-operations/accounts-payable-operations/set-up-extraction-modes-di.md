---
title: Configure data extraction modes
description: Configure the extraction modes for use cases to define how Document Intelligence extracts fields from documents.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Data extraction]
breadcrumb: [Configure Document Intelligence using Now Assist for Accounts Payable Operations \(APO\), Configure Now Assist for Accounts Payable Operations \(APO\), Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Configure data extraction modes

Configure the extraction modes for use cases to define how Document Intelligence extracts fields from documents.

## Before you begin

Role required: sn\_docintel.manager

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the workflow group, select &gt; **Finance and Supply Chain** &gt; **Invoice data extraction** to view the skills for the APO features.

3.  Select the settings ![docintel settings](../image/icon-docintel-settings-gear.png) icon.

4.  Select the extraction mode for the use case**Accounts Payable Operations**.![Extraction mode](../image/settings-na.png)

5.  Adjust the DocIntel full automation mode.

    -   When Full automation mode is turned on, DocIntel automatically completes and submits the document task. The required values or fields in the invoice document are auto-filled or identified as missing in the document. If there are no fields defined as required for the document task, then DocIntel automatically completes and submits the document task.
    -   When you turn on the **Any required field is missing in the document**, the full automation mode is turned off and requires an agent review.
6.  Select **Save**.


