---
title: Currencies and budget reference rates
description: The support for use of multiple currencies provides conversions for budget items in different currencies.
locale: en-US
release: australia
product: PPM Collaboration
classification: ppm-collaboration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PPM Standard \(Project Portfolio Management\), Explore Project Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Currencies and budget reference rates

The support for use of multiple currencies provides conversions for budget items in different currencies.

## Currency support

The application can use a base currency, also called the reporting currency that you specify with system properties. You can also specify other currencies for budgets and budget items.

<table id="table_ygy_xz2_2t"><thead><tr><th>

Item

</th><th>

Currency used

</th></tr></thead><tbody><tr><td>

Budget plan

</td><td>

A currency that you specify on the Budget Plan form. When the plan is converted to a forecast, the application converts the currency to the reporting currency.

</td></tr><tr><td>

Budget plan items

</td><td>

A currency that you specify on the Budget Item form.If the budget plan item has currency different from the budget plan currency, the budget plan item amount is converted to the budget plan currency.

</td></tr><tr><td>

Budget forecast

</td><td>

The reporting currency.

</td></tr></tbody>
</table>## Budget reference rates

Budget reference rates are exchange rates between currencies. Each reference rate is valid for a specified time period. The application uses budget reference rates when budget items are in a different currency from the budget plan and forecast. The application automatically converts budget item currency values to a global system currency value when it calculates the Budget Amount on a Budget Plan, and when it shows values on budget forecasts.

**Note:** Currency support is for budgets only. You cannot create allocations in multiple currencies.

**Parent Topic:**[PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/concept/c_ProjectPortfolioSuiteWithFinancials.md)

**Related topics**  


[Activate Investment Funding for projects and demands](../../investment-funding/task/activate-investment-funding-ppm.md)

