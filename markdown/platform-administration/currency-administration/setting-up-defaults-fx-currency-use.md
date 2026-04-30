---
title: Setting up defaults required for FX Currency use
description: Set up the defaults required for use of FX Currency fields in your instance.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Setting up defaults required for FX Currency use

Set up the defaults required for use of FX Currency fields in your instance.

Perform the following setup tasks to enable FX Currency processing:

-   **[Add conversion rates using a custom rate table](../task/custom-rate-table.md)**  
You can create a custom rate table to ensure repeatable and consistent calculations. In a custom rate table, you control the conversion rates and the frequency of rate conversions. If you don't define custom rate tables, FX Currency fields use the System Conversion Currency Rate \[fx\_system\_rate\] table, which updates rates daily from the ECB \(European Central Bank\) website.
-   **[Configuring FX Currency global settings](../task/fx-currency-configure.md)**  
Before setting up and using FX Currency, review the related system properties to confirm or modify its default behavior.
-   **[Add an FX Currency field to a table](../task/add-fx-currency-field-table.md)**  
Before using and configuring an FX Currency field, you first add it an existing table, or to a new one, in **System Definition** &gt; **Tables.**
-   **[Configuring FX Currency field behavior](configure-fx-currency-field-behavior.md)**  
After establishing global currency defaults, you can create custom FX Currency configurations for specific table fields. Identify the table fields that use FX Currency, and define how currency conversion calculations should be performed, displayed, filtered, and aggregated.
-   **[Update a Currency Instance record](../task/updating-fx-currency-instance-record.md)**  
Review and edit the details of a currency entry in an FX Currency field.

**Parent Topic:**[Configuring currency fields](configure-currency-admin.md)

**Related topics**  


[Setting up defaults required for standard currency use](setting-up-standard-currency-defaults.md)

