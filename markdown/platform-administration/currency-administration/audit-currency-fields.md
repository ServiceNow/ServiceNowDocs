---
title: Configure default currency fields in audit records
description: You can control what currency value is stored in audit records.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer]
---

# Configure default currency fields in audit records

You can control what currency value is stored in audit records.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Find **glide.sys.audit\_currency\_value**, and set to the desired value.

    |Value|Description|
    |-----|-----------|
    |false|Value entered in the audit record is the numeric value in the session currency. It does not include the currency code. This value is the default.|
    |true|Value as entered by the user in the format USD. For example, 1234.56.|


**Parent Topic:**[Setting up defaults required for standard currency use](../concept/setting-up-standard-currency-defaults.md)

