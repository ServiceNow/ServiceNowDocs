---
title: Schedule the rate update job
description: Schedule the ECB Exchange Rate Load to perform a nightly download of currency-conversion tables from the European Central Bank.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Default currency conversions, Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer]
---

# Schedule the rate update job

Schedule the ECB Exchange Rate Load to perform a nightly download of currency-conversion tables from the European Central Bank.

## Before you begin

Role required: admin

## About this task

You can adjust the frequency of this behavior or disable it entirely. For information about turning off the regularly scheduled update and maintaining the Exchange Rate table manually, see [Use your own currency-conversion rates](t_UseYourOwnConversionTable.md) and [FX Currency fields](../../currency/concept/fx-currency.md).

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Open the job named **Retrieve System Rates**.

3.  Modify the schedule, as needed.

    After the job runs, it stores and loads the rates from the Exchange Rate \[fx\_rate\] table. Navigate to **System Localization** &gt; **Exchange Rates** to see them.


**Parent Topic:**[Default currency conversions](../../currency/concept/currency-conversions.md)

