---
title: Configuring FX Currency field behavior
description: After establishing global currency defaults, you can create custom FX Currency configurations for specific table fields. Identify the table fields that use FX Currency, and define how currency conversion calculations should be performed, displayed, filtered, and aggregated.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up defaults required for FX Currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring FX Currency field behavior

After establishing global currency defaults, you can create custom FX Currency configurations for specific table fields. Identify the table fields that use FX Currency, and define how currency conversion calculations should be performed, displayed, filtered, and aggregated.

For each selected field that uses FX Currency, you configure settings that:

-   Govern decimal precision and currency display in lists, forms, and reports.
-   Identify the reference currency code for converting currency values entered into an FX Currency field into a common currency for report aggregations.
-   Identify the rate table and data source to use for currency conversions.
-   Specify the rate and target fields to use for filtering custom conversion rates.

**Note:** When you create a currency configuration, it applies those settings only to the FX Currency field that you add it to. An FX Currency configuration takes precedence over global system properties that you established in **System Localization** &gt; **All Properties.**

To learn more about global currency defaults, see [Configuring FX Currency global settings](../task/fx-currency-configure.md).

You can change the defaults at any time. Doing so doesn't affect existing values, but it can make working with existing values difficult.

-   For example, if you modify the **Reference Currency** field in the Currency tab, existing instance records have the old reference currency, but new instance records have the new reference currency. You can't perform an operation such as sum aggregation because the reference values are in different currencies.
-   However, because the actual reference currency in the Currency Instance \[fx\_currency2\_instance\] table is accessible in an FX Currency field, you can use any script that performs this aggregation.

-   **[Identify the FX Currency field and its display parameters](../task/fx-currency-display-parameters.md)**  
Specify the table, and the field within the table \(for example, cost\), that the FX Currency configuration applies to. Then, select the decimal precision and currency display parameters for the field.
-   **[Set the reference currency](../task/fx-currency-set-reference.md)**  
Set the reference currency for the designated FX Currency field. The ServiceNow AI Platform uses the reference currency to convert values entered into the FX Currency field into a common currency for report aggregation purposes.
-   **[Specify the rate table and date source for currency conversions](../task/fx-currency-conv-rate-table-date-source.md)**  
Identify the rate table and data source to use for currency conversions for the designated FX Currency field.
-   **[Select the rate and target table fields used for filtering](../task/fx-currency-rate-target-table-fields.md)**  
Optionally specify the rate table and target table fields to use for filtering conversion rate information.

**Parent Topic:**[Setting up defaults required for FX Currency use](setting-up-defaults-fx-currency-use.md)

**Related topics**  


[Add conversion rates using a custom rate table](../task/custom-rate-table.md)

[Configuring FX Currency global settings](../task/fx-currency-configure.md)

[Add an FX Currency field to a table](../task/add-fx-currency-field-table.md)

[Updating the Currency Instance record](../task/updating-fx-currency-instance-record.md)

