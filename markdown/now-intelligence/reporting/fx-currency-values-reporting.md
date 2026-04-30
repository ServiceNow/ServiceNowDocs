---
title: FX Currency values in reporting
description: Manage projects in multiple currencies with FX \(Foreign Exchange\) Currency. You can report on the projects in currency values entered by the user, a reference currency, or both.When you report on FX Currency fields, there are certain limitations that may generate errors. These errors are associated with aggregation.When you report on FX Currency tables, some combinations of group and aggregation type are not possible to calculate. These combinations return the message 'Cannot generate the report. There are mismatched currency codes. Change your aggregation source or filter conditions.'
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [FX Currency, Cannot generate report mismatched currency codes.]
breadcrumb: [Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# FX Currency values in reporting

Manage projects in multiple currencies with FX \(Foreign Exchange\) Currency. You can report on the projects in currency values entered by the user, a reference currency, or both.

**Note:** You don't have to install a plugin to use FX Currency functionality. It's activated by default.

FX Currency functionality is described in detail in . In the context of reporting, it is important to aggregate on the reference currency which the other currencies are converted to.

**Note:** When there are multiple currencies, calculations may not be possible. Change your aggregation source or filter conditions to show the report.

When you aggregate by **Average** or **Sum** on an FX currency field, you choose the **Aggregation Source**.

-   **Use FX currency configuration**

    Calculates the values based on the FX Currency Configuration table. For more information, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **As entered values**

    Calculate values based on currency values entered by the user.

    **Note:** If you select this option, you may experience situations where amounts entered in different currencies can't be properly aggregated. For example, if there are currency amounts in US Dollars, Yen, and Euros. It is only possible to aggregate values on one currency at a time. If you aggregate records in different currencies, this error displays: 'Cannot generate the report. There are mismatched currency codes.' See [Mismatched currency example](fx-currency-values-reporting.md#).

-   **Reference values**

    Calculates the values based on the reference currency.


**Parent Topic:**[Advanced reporting topics](c_AdvancedReporting.md)

## Report on FX currency fields

When you report on FX Currency fields, there are certain limitations that may generate errors. These errors are associated with aggregation.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Create New**.

2.  On the **Data** tab, name the report, choose the source table with FX currency fields, and then click **Next**.

    The source must have FX Currency fields. See [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  On the **Type** tab, choose the visualization type that you want to use.

    See [Report types](../reference/report-types-creation-details-rd.md).

4.  On the **Configure** tab, choose how you want to group, stack, and aggregate the report.

    It is only possible to aggregate values on one currency at a time. If you aggregate records in different currencies on an FX Currency field, this error displays: "Cannot generate the report. There are mismatched currency codes."


## Mismatched currency example

When you report on FX Currency tables, some combinations of group and aggregation type are not possible to calculate. These combinations return the message 'Cannot generate the report. There are mismatched currency codes. Change your aggregation source or filter conditions.'

The source of this report has costs in euros, Japanese yen, and British pounds. This visualization aggregates costs by count distinct, meaning that each individual value gets its own segment.

![FX currency example with count distinct aggregation](../image/fx-currency-count-distinct.png)

When you try to aggregate costs in multiple currencies by sum or average, there are several possible outcomes.

-   **Aggregation Source is Use FX Currency configuration**

    It is not possible to perform the calculation, because the currencies are mismatched.

-   **Aggregation Source is As entered values**

    Usually the entered values are in multiple currencies as well and it is not possible to perform the calculation.

-   **Aggregation Source is Reference values**

    In this case, the values are converted to the reference value before calculation and the report is generated. For more information, see [Understanding FX Currency values in forms](https://www.servicenow.com/docs/access?context=fx-currency-values-forms&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


