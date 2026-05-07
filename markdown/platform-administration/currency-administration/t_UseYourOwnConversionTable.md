---
title: Use your own currency-conversion rates
description: All currency conversions are based on the rates stored in the Exchange Rate table. You can turn off the regularly scheduled update from the European Central Bank \(ECB\), and maintain the table manually.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default currency conversions, Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Use your own currency-conversion rates

All currency conversions are based on the rates stored in the Exchange Rate table. You can turn off the regularly scheduled update from the European Central Bank \(ECB\), and maintain the table manually.

## Before you begin

Role required: admin

## About this task

Daily exchange rates are loaded in the Exchange Rate \[fx\_rate\] table automatically using the [Euro foreign exchange reference rates](http://www.ecb.int/stats/eurofxref/eurofxref-daily.xml) from the ECB and the Update Currency Conversion Rates scheduled job.

If ECB does not supply the daily rates for a specific currency, you can manually enter rates into the Exchange Rate table. Use an import set or another service \(for example, JSON or SOAP\) that supports uploading additional currency rates. You can then add a scheduled job similar to the Update Currency Conversion Rates scheduled job to update these currencies.

**Note:** The Update Currency Conversion Rates job replaced the ECB Exchange Rate Load and Retrieve System Rates jobs, which are turned off by default. They must remain turned off to use custom conversion rates.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the job named **Update Currency Conversion Rates**.

3.  Clear the **Active** option.

4.  Select **Update**.

5.  Enter new exchange rates either manually or with an import set.


**Parent Topic:**[Default currency conversions](../../currency/concept/currency-conversions.md)

