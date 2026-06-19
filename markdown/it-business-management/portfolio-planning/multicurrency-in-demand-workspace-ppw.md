---
title: Multicurrency in Next Experience for Demand Management
description: Manage and track demand financials in your corporate currency, regional currency, or project currency using the multicurrency feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/multicurrency-in-demand-workspace-ppw.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Multicurrency in Next Experience for Demand Management

Manage and track demand financials in your corporate currency, regional currency, or project currency using the multicurrency feature.

## Overview of multicurrency

In global organizations, demands are often managed at one location and executed at another. Each location might use different currencies for budget spending, making it difficult to monitor and track financials.

The multicurrency feature in Next Experience for Demand Management enables you to manage and track demands from any geographic location in any currency. You can monitor demand financials in one defined currency, such as your functional currency or regional currency, while tracking the budget in another. You can also manage your demands in one currency and specify a different currency for managing your future projects.

## Activation information

To enable multicurrency features in Next Experience for Demand Management, activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin. This activation:

-   Enables the demand currency view in demand, cost plan, and benefit plan forms.
-   Enables you to manage simple demand financials, cost plans, benefit plans, and budgets in the demand currency
-   Automatically activates the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin, giving you the option to switch between the default view and demand currency view

## Currency preferences

You can specify your currency preference for managing demand financials: a functional currency, a regional currency, or a local currency. For more information, see [Select demand currency preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/select-demand-currency-preference-ppw.md).

## Demand currency view

The Demand Currency view displays multicurrency fields in addition to the standard demand form fields. Enable this view from the form context menu.

You can designate a currency other than the functional currency as the processing demand currency. The **Demand currency** field appears on the Financials section of the Demand form, where you can select any active currency from the Currencies \[fx\_currency\] table.

**Note:** The Demand currency field is set to read only after you create a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown for the demand.

