---
title: Life cycle of records containing FX Currency fields
description: The behavior of FX Currency fields varies during the processing that occurs during the lifetime of a record containing them.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Life cycle of records containing FX Currency fields

The behavior of FX Currency fields varies during the processing that occurs during the lifetime of a record containing them.

## Insert / Update

The FX Currency field points to a Currency Instance \[fx\_currency2\_instance\] record. When you change the currency value in an FX Currency field, it determines the conversion rate and calculates the reference currency before:

-   The **before** business rules run.
-   The **after** business rules run, and it includes any further changes you may have made to the **before** business rules.

**Note:** If the FX Currency field contains an invalid currency code, an exception condition may appear before these two stages occur.

## Auditing

Since an FX Currency field points to a Currency Instance record that stores multiple values, the audit string is a composite that contains this information. The string stored in the System Audit \[sys\_audit\] table is in the format of `EUR;111.222;4555525f5553445f3230313931323033`, with the following values, separated by semicolons:

-   Three letter ISO currency code. For example, `EUR`.
-   Amount as an unformatted number. For example, `111.222`.
-   System identifier \(sys\_id\) for the conversion rate record in the Currency Conversion Rate \[fx\_conversion\_rate\] table. For example, `4555525f5553445f3230313931323033`.

When creating history lines for a user, the audited string is formatted, using the locale of the user. It's in the format of `€111.22;2019-12-03 17:00:00-3000-01-01 23:59:59;fx_system_rate`, with the following values, separated by semicolons:

-   Formatted currency string in the user locale. For example, `€111.22`.
-   Start span-End span, as expressed in the conversion rate record in the System Rate \[fx\_system\_rate\] table. For example, `2019-12-03 17:00:00-3000-01-01 23:59:59`.
-   Name of the conversion rate table. For example, `fx_system_rate`.

**Parent Topic:**[Currency administration references](currency-admin-references.md)

**Related topics**  


[Dot-walkable Currency Instance fields](fx-currency-dot-walkable-fields.md)

