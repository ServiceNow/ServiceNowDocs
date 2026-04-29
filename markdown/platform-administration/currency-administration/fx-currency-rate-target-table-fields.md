---
title: Select the rate and target table fields used for filtering
description: Optionally specify the rate table and target table fields to use for filtering conversion rate information.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [FX Currency field behavior, Defaults required for FX Currency use, Configure, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Select the rate and target table fields used for filtering

Optionally specify the rate table and target table fields to use for filtering conversion rate information.

## About this task

For example, you maintain interfaces to several ERP systems, have currency conversion rates that are unique to each ERP, but you maintain all rates in a single table.

-   To identify rates for a specific ERP system, there is a **System** field in the rate table that contain entries identifying each ERP system, for example, ABC, XYZ. In the target table with the FX Currency field, you have a similarly named field for identifying the conversion rates required for specific ERP systems.
-   When you perform currency conversions, and the rate and target table field entries match, it uses the rates that are unique to that specific ERP.

## Procedure

1.  Click the Rate Filter tab.

2.  In the **Rate Table Field** field, select the field in the rate table to match against the specified target table field for conversion rate filtering.

    Select **--None--** skip use of a rate table field for conversion rate filtering.

3.  In the **Target Table Field** field, select the field in the target table to match against the specified rate table field for rate filtering.

    Select **--None--** skip use of a target table field for rate filtering.

4.  Click **Save**.


**Parent Topic:**[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

**Related topics**  


[Understanding FX Currency values in lists and reports](../concept/fx-currency-values-lists-reports.md)

[Understanding FX Currency values in forms](../concept/fx-currency-values-forms.md)

