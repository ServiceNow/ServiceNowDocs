---
title: Set the reference currency
description: Set the reference currency for the designated FX Currency field. The ServiceNow AI Platform uses the reference currency to convert values entered into the FX Currency field into a common currency for report aggregation purposes.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FX Currency field behavior, Defaults required for FX Currency use, Configure, Currency administration, Configure core features, Administer]
---

# Set the reference currency

Set the reference currency for the designated FX Currency field. The ServiceNow AI Platform uses the reference currency to convert values entered into the FX Currency field into a common currency for report aggregation purposes.

## Before you begin

Roles required: admin

## Procedure

1.  Click the Currency tab.

2.  In the **Reference Currency** field, select the three-digit ISO currency code used for the reference currency.

    For example, select **USD** if the currency values expressed in various currencies convert into US Dollars for report aggregation.

    To use the global reference currency default you established in the **glide.currency2.default\_reference\_currency** property in **System Localization** &gt; **All Properties.**

3.  In the **Reference Currency Source** field, designate the source of the reference currency.

    -   To use as the source of its reference currency when creating or updating a currency value for this FX Currency field, select the dot-walked field.
        -   For example, `Cost` is an FX Currency field, and `my_currency` is a reference or string field in the Currency \[fx\_currency\] table that contains a currency code such as USD.
        -   When you create an FX Currency configuration for the `Cost` field, you select `my_currency` as its reference currency.
    -   If you do not want to select the reference currency from another field, select **--None--**.
4.  Click **Save**.


**Parent Topic:**[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

