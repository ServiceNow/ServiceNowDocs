---
title: Use your own currency-conversion rates
description: All currency conversions are based on the rates stored in the Exchange Rate table. You can turn off the regularly scheduled update from the European Central Bank \(ECB\), and maintain the table manually.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Default currency conversions, Setting up defaults required for standard currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Use your own currency-conversion rates

All currency conversions are based on the rates stored in the Exchange Rate table. You can turn off the regularly scheduled update from the European Central Bank \(ECB\), and maintain the table manually.

## Before you begin

Role required: admin

## About this task

ECB Exchange Rate Load loads exchange rates from the ECB for the following currencies:

[http://www.ecb.int/stats/eurofxref/eurofxref-daily.xml](http://www.ecb.int/stats/eurofxref/eurofxref-daily.xml).

If ECB does not supply the daily rates for a specific currency, you can manually enter rates into the Exchange Rate table. Use an import set, or another service \(for example, JSON or SOAP\) that offers upload of more currency rates. You can then add a similar scheduled job to update these currencies.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Open the job named **ECB Exchange Rate Load**.

3.  In the Trigger type field, select **-- None --**.

4.  Enter new exchange rates either manually or with an Import Set.


**Parent Topic:**[Default currency conversions](../../currency/concept/currency-conversions.md)

