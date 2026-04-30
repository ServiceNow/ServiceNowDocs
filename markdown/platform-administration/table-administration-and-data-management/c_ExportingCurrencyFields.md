---
title: Exporting currency fields to Excel
description: Exporting currency fields to Excel applies Account formatting and can be configured to convert all values to US dollars or to export values in the user's session currency.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer]
---

# Exporting currency fields to Excel

Exporting currency fields to Excel applies Account formatting and can be configured to convert all values to US dollars or to export values in the user's session currency.

When exporting currency fields to Microsoft Excel, the cells containing currency data use Accounting formatting. This formatting allows you to perform numeric operations on those values as well as view the currency symbol, such as $ or €.

When exporting currency fields the type of currency, such as $ or €, is preserved by default. The conversion rates for non-USD currencies are stored on the Exchange Rates \[fx\_rate\] table.

You can choose to export all currency values either in US dollars or in the user's session currency.

-   To export all currency values in US dollars, set the property **glide.excel.fixed\_currency\_usd** to **true**.
-   To export all currency values in the user's session currency, set the property **glide.excel.convert\_to\_user\_currency** to **true**.

If both **glide.excel.fixed\_currency\_usd** and **glide.excel.convert\_to\_user\_currency** are set to **true**, **glide.excel.fixed\_currency\_usd** overrides **glide.excel.convert\_to\_user\_currency**.

## Currency export behavior and symbols

The behavior of the currency field in Excel depends on the **Symbol** of the currency.

-   When the currency symbol is $, the Excel cell type is set as **Currency**.
-   When the currency symbol is 1 character \(such as ¥ or ¢\) or more than 1 character \(such as KR\), the Excel cell type is set to **Custom**.

**Related topics**  


[Currency administration](../../currency/concept/currency.md)

[Single-currency mode](../../currency/concept/single-currency-mode.md)

[Control default currency field configuration and use in an instance](../../currency/reference/currency-properties.md)

