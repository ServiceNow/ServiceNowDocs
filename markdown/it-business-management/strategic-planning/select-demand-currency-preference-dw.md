---
title: Select demand currency preference
description: Set your currency preference for managing and tracking demand financials from the functional currency, regional currency, or local currency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/select-demand-currency-preference-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multicurrency in demands, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Select demand currency preference

Set your currency preference for managing and tracking demand financials from the functional currency, regional currency, or local currency.

## Before you begin

The PPM Standard Multicurrency feature must have been installed. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ppm-collaboration/t_ActivateProjectPortfolioSuiteWithFinancials.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Preferences-Project**.

2.  From the Demand currency setup list, select a currency option.

<table id="choicetable_lc1_qht_dnb"><thead><tr><th align="left" id="d59216e98">

Demand currency preference

</th><th align="left" id="d59216e101">

Currency option

</th></tr></thead><tbody><tr><td id="d59216e107">

**Manage demands using the functional currency**

</td><td>

**Follow functional currency**: Manage demands using your organization's functional currency. When you create a project from the demand, the project currency carries over to the Project form. You can change the project currency later.For example, if your functional currency is USD, both demands and projects use USD.

</td></tr><tr><td id="d59216e121">

**Manage demands using the same currency as the project currency**

</td><td>

**Drive project currency**: Manage demands and projects using the same currency. This currency can be your functional currency or any other currency. For example, to manage demands and projects in GBP, select this option and specify GBP as your demand currency. The **Project Currency** field in the demand form automatically populates with GBP when you save the form.

</td></tr><tr><td id="d59216e137">

**Manage demands and projects in different currencies**

</td><td>

**Flexi**: Manage your demands and projects created from the demand using different currencies. For example, to manage demands in USD and projects in GBP, select this option and specify USD as the demand currency and GBP as the project currency.

</td></tr></tbody>
</table>3.  Select **Save**.


## What to do next

Enable the multicurrency view in the demand form and other demand-related forms. For more information, see [Enable the demand currency view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/enable-demand-currency-view-dw.md).

