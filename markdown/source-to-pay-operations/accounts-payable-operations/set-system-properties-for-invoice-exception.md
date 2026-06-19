---
title: Set system properties for invoice exception
description: Set the maximum parallel threads system property \( sn\_ap\_apm.exception.engine.max\_parallel\_thread\_count \) to optimize the performance of the exception engine scheduler in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/set-system-properties-for-invoice-exception.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, Accounts Payable Operations, invoice exception, invoice processing, admin]
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Set system properties for invoice exception

Set the maximum parallel threads system property \(`sn_ap_apm.exception.engine.max_parallel_thread_count`\) to optimize the performance of the exception engine scheduler in Accounts Payable Operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  Search for **All properties** under **System properties**.

3.  Search for `sn_ap_apm.exception.engine.max_parallel_thread_count` and open the system property.

    \[Omitted image "apo-system-properties.png"\] Alt text: System properties of APOThe system property `sn_ap_apm.exception.engine.max_parallel_thread_count` opens as a record. The **Value** field displays the default value as 4. This value indicates 4 worker threads of your instance will be used by the exception engine scheduler when it executes. You can edit the record in editing mode.

4.  In the **Value** field, you can enter the value as 6, or 8.

    The exception engine scheduler makes use of 6 or 8 worker threads in your instance when it executes. This is recommended only when you have more than 2 nodes, i.e more than 16 worker threads.

5.  Select **Update**.


