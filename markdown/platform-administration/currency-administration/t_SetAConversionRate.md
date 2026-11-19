---
title: Schedule the rate update job
description: Schedule the Update Currency Conversion Rates job to perform a nightly download of currency-conversion tables from the European Central Bank.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/currency-administration/t\_SetAConversionRate.html
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default currency conversions, Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer]
---

# Schedule the rate update job

Schedule the Update Currency Conversion Rates job to perform a nightly download of currency-conversion tables from the European Central Bank.

## Before you begin

Role required: admin

## About this task

You can adjust the frequency of this behavior or turn it off it entirely. For information about turning off the regularly scheduled update and maintaining the Exchange Rate table \[fx\_rate\] manually, see [Use your own currency-conversion rates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/currency-administration/t_UseYourOwnConversionTable.md) and [FX Currency fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/currency-administration/fx-currency.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the job named **Update Currency Conversion Rates**.

3.  Modify the schedule, as needed.

    After the job runs, it stores and loads the rates from the Exchange Rate table. Navigate to **System Localization** &gt; **Exchange Rates** to see the exchange rates.


**Parent Topic:**[Default currency conversions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/currency-administration/currency-conversions.md)

