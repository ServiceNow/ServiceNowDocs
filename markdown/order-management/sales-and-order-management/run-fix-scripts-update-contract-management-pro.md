---
title: Run fix scripts to update Contract Management Pro
description: Manually run fix scripts after you have installed the demo data.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with Contract Management Pro, Configuring Quote Management, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Run fix scripts to update Contract Management Pro

Manually run fix scripts after you have installed the demo data.

## Before you begin

Role required: admin

## About this task

If the demo data was installed, the Request Type field in the demo data will remain blank. Consequently, the field may not display the correct value to distinguish between new contracts and amendments. To fix this, run the Populate Request Type script in CMR to ensure the request type is set correctly.

## Procedure

1.  Navigate to **All** &gt; **Fix Script**.

2.  Search for Populate Request type in Contract document revision \(CMR\) and open the record.

3.  Click **Run Fix Script** at the top of record, in the modal that opened up select **Proceed/Proceed in background** to run the script.


