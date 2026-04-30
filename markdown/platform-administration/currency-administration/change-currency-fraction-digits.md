---
title: Change default currency decimal places
description: You can specify the number of decimal places stored and used in currency fields and calculations.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up defaults required for standard currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Change default currency decimal places

You can specify the number of decimal places stored and used in currency fields and calculations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Find **glide.currency\_price.use\_all\_fraction\_digits**, and set to the desired value.

    |Value|Description|
    |-----|-----------|
    |false|Uses two decimal places.|
    |true|Uses four decimal places. This value is the default.|


**Parent Topic:**[Setting up defaults required for standard currency use](../concept/setting-up-standard-currency-defaults.md)

