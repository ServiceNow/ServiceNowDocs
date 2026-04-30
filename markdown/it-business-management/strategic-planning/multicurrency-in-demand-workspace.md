---
title: Multicurrency in Next Experience for Demand Management
description: Manage and track demand financials in your corporate currency, regional currency, or project currency using the multicurrency feature.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-02-04"
reading_time_minutes: 2
breadcrumb: [Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Multicurrency in Next Experience for Demand Management

Manage and track demand financials in your corporate currency, regional currency, or project currency using the multicurrency feature.

## Overview of multicurrency

In global organizations, demands are often managed at one location and executed at another. Each location might use different currencies for budget spending, making it difficult to monitor and track financials.

The multicurrency feature in Next Experience for Demand Management lets you manage and track demands from any geographic location in any currency. You can monitor demand financials in one currency while spending the budget in a different currency, such as your functional currency or regional currency. You can also manage your demands in one currency and specify a different currency for managing your future projects.

## Activation information

To enable multicurrency features in Next Experience for Demand Management, activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin. This activation:

-   Enables the demand currency view in demand, cost plan, and benefit plan forms.
-   Enables you to manage simple demand financials, cost plans, benefit plans, and budgets in the demand currency
-   Automatically activates the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin, giving you the option to switch between the default view and demand currency view

## Currency preferences

After activating the plugin, specify your currency preference for managing demand financials. You can select your functional currency, a regional currency, or a local currency. For more information, see [Select demand currency preference](../task/select-demand-currency-preference-dw.md).

## Demand currency view

The Demand Currency view displays multicurrency fields in addition to the standard demand form fields. Enable this view from the form context menu.

You can designate a currency other than the functional currency as the processing demand currency. The **Demand currency** field appears on the Financials section of the Demand form, where you can select any active currency from the Currencies \[fx\_currency\] table.

**Note:** The Demand currency field becomes read only once you create a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown for the demand.

## Multicurrency in demand tasks

Track expenses for demand tasks in demand currency. When a time card for a demand task is submitted and processed, the actual cost is calculated based on the rate model, default labor rate, or system property rate. View this actual cost in the Demand Task form in the **Demand currency** and **Actual cost in demand currency** fields.

## Multicurrency in demand baselines

Compare financial baselines to track demand performance over time. Baseline comparison helps you identify and review financial changes made to the demand at various life-cycle stages. With the multicurrency feature, you can view financial information in demand currency when comparing baselines. You can also configure the baseline view to add fields and view details in demand currency. For more information, see [Create financial baselines](../task/create-compare-financial-baselines-dw.md).

