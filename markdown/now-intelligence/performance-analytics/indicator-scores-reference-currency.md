---
title: Indicator scores in reference currency
description: You can track the trends for monetary fields of the types Price, Currency, or FX Currency. The scores for an indicator based on any of these fields are collected in the Reference Currency values.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indicator scores in reference currency

You can track the trends for monetary fields of the types Price, Currency, or FX Currency. The scores for an indicator based on any of these fields are collected in the Reference Currency values.

To collect these scores, select the unit on the indicator as **Use reference currency**

**Warning:** If the reference currency for a field changes after you have set up the indicator, scores are no longer collected properly.

Sometimes you need to provide your users with monetary KPIs converted to a standard currency. Consider a global project manager or CFO who deals with project costs in many different original currencies. They need to see all these costs converted to the global company currency so they can make decisions based on global trends. To provide such users with the KPIs they need, you can configure Performance Analytics indicators to collect scores denominated in a reference currency.

To collect indicator scores in a reference currency, create an indicator with the following characteristics:

-   The indicator is an [automated indicator](performance-analytics-glossary.md#), not a formula or a manual indicator.
-   The aggregate is not **Count** or **Count Distinct** and the indicator is not **Scripted**.
-   The selected **Field** to aggregate has the type Price, Currency, or FX Currency.
-   The selected **Unit** for the scores is **Use reference currency**.

For the full procedure of creating such an indicator, see [Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#).

**Note:**

-   A currency administrator must configure FX Currency fields before you use them in indicators.
-   The **Precision** field is not available on the indicator form when **Use reference currency** is selected. Instead, the precision is inherited from the FX Currency configuration.

After the scores have been collected, you can explore them more deeply in the Analytics Hub or share them through a widget. The reference currency precision and symbol are used in all visual elements: the score value, change value, target, threshold, and tooltips.

## System Reference Currency reference

As a Performance Analytics expert, you do not set up the reference currency. Someone with a currency administrator role performs this task. However, you may still want to know how reference currencies work on the ServiceNow AI Platform. A brief summary with links follows.

For a Price or Currency field, the system reference currency is the value of **glide.system.locale** as set in the localization properties. If this property is not set, the system default based on physical location is used. For more information about setting the reference currency for these fields, see [Setting up and operating standard currency fields](https://www.servicenow.com/docs/access?context=configure-and-use-default-currency-fields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** Performance Analytics indicators do not use session currency values.

For an FX Currency field, the indicator scores are based on this hierarchy of configuration settings:

1.  If field-level FX Currency configurations are set, these take precedence. If they are not set...
2.  The Global FX Currency configuration is used. If the global configuration is not set...
3.  The setting in **glide.system.locale** is used. If no value is set in this property...
4.  The system default is used.

For more information about configuring FX Currency fields, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

