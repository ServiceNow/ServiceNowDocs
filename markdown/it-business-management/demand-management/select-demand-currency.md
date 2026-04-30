---
title: Select demand currency preference
description: Set your currency preference to use for managing and tracking the financials of your demands from the functional currency, regional currency, or local currency.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Select demand currency preference

Set your currency preference to use for managing and tracking the financials of your demands from the functional currency, regional currency, or local currency.

## Before you begin

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Preferences-Project**.

2.  Select a currency option for managing your demands from the Demand currency setup list.

<table id="choicetable_lc1_qht_dnb"><thead><tr><th align="left" id="d158119e82">

Demand currency preference

</th><th align="left" id="d158119e85">

Currency Option

</th></tr></thead><tbody><tr><td id="d158119e91">

**Manage demands using the functional currency**

</td><td>

Select the **Follow functional currency** option to manage your demands using the functional currency of your organization. The project currency is carried over to the Project form when you create a project from the demand in the future. ​You can change the project currency for managing your projects later.For example, if the functional currency of your organization is USD, then USD is set as the currency for both demands and projects.

</td></tr><tr><td id="d158119e106">

**Manage demands using the same currency as the project currency**

</td><td>

Select the **Drive project currency** option to manage your demands and projects using the same currency. This currency can be your functional currency or any other currency. For example, if you want to manage your demand and project in a local currency, say GBP, then you would select this option and specify GBP as your demand currency​. The **Project Currency** field in the demand form is automatically populated with GBP as your project currency on saving the form.

</td></tr><tr><td id="d158119e124">

**Manage demands and projects in different currencies**

</td><td>

Select **Flexi option** to manage your demands and projects, created from the demand, using different currencies. For example, if you want to manage your demands and projects in different currencies such as USD and GBP, then you would select this option and specify USD as demand currency and GBP as your project currency respectively​.

</td></tr></tbody>
</table>3.  Select **Save**.


## What to do next

Enable the multicurrency view in the Demand and other demand-related forms. For more information, see [Enable demand currency view](enable-multicurrency-demand.md).

**Parent Topic:**[Multicurrency in Demand Management](../concept/multicurrency-demand.md)

