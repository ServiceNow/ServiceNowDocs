---
title: Configure the currency optimizer
description: You can configure the system to use an optimizer for currency/price fields to speed up list view \(reading currency/price values\).
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up defaults required for standard currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the currency optimizer

You can configure the system to use an optimizer for currency/price fields to speed up list view \(reading currency/price values\).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  To turn on the currency optimizer, find **glide.currency\_price\_optimizer.enabled**, and set to the desired value.

    |Value|Description|
    |-----|-----------|
    |false|Optimizer is not used.|
    |true|Optimizer is used. This value is the default.|

3.  To set the minimum number of rows needed by the currency optimizer, find **glide.currency\_price\_optimizer.min\_rows**, and set to the desired value.

    The default value is 4.


**Parent Topic:**[Setting up defaults required for standard currency use](../concept/setting-up-standard-currency-defaults.md)

