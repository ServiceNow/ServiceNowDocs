---
title: Multicurrency in Demand Management
description: Manage and track the financials of your demands in the corporate currency, regional currency, or the same currency that you want to use for managing the project using the multicurrency feature. The corporate policy typically governs the choice of this preference.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Multicurrency in Demand Management

Manage and track the financials of your demands in the corporate currency, regional currency, or the same currency that you want to use for managing the project using the multicurrency feature. The corporate policy typically governs the choice of this preference.

In a global or multinational organizations, demands are often managed and tracked at one geographic location and executed at a different geographic location. As each location might use a different currency to spend the budget, this difference in geographic location makes it difficult to monitor and track financials for such demands.

The multicurrency feature in Demand Management makes it easier for you to manage and track your demands from any geographical location in any currency. You can monitor and track the financials of your demands in one currency and spend the budget in a different currency such as functional currency, regional currency, or a currency that you want to later use to manage your projects. You can also choose to manage your demands in one currency and specify a different currency for managing your future projects.

## Activation information

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin to enable the multicurrency features in Demand Management. Activating the plugin enables the demand currency view in demand, cost plans, and benefit plans forms. With the demand currency view, you can manage your simple demand financials, cost plans, benefit plans, and budgets in the demand currency.

**Note:** Activating this plugin automatically activates the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin and therefore you get the option to switch between the default view and the demand currency view.

## Currency Preferences

After activating the multicurrency plugin, specify your currency preference for managing your demand financials. You can select your functional currency, a regional currency, or a local currency. For more information, see [Select demand currency preference](../task/select-demand-currency.md).

## Demand currency view

In addition to the default view in the Demand form, the Demand Currency view enables you to view the multicurrency fields. You can enable this view from the form context menu.

You can designate a currency other than the functional currency as the processing Demand Currency for a demand. The **Financials** tab of the Demand form has the **Demand currency** field. You can select an active currency from the Currencies \[fx\_currency\] table.

**Note:**

The **Demand currency** field of a demand becomes read-only once you create a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown for the demand.

## Multicurrency in Demand Tasks

Track the expenses incurred while performing the demand tasks in demand currency. When the time card for a demand task is submitted and processed, the actual cost is calculated based on the rate model, the default labor rate, or the rate defined in the system property. You can view this actual cost in the Demand Task form in the **Demand currency** and **Actual cost in demand currency** fields. For more information, see [Demand tasks](demand-task.md).

## Multicurrency in Demand Baseline

Compare the financial baselines of your demands to track the performance of a demand over time. Baseline comparison enables you to identify and review the financial changes made to the demand at various stages of the demand life cycle. With the multicurrency feature, you can view the financial information in the demand currency when you compare the baselines. You can also configure the baseline view to add additional fields and view details in demand currency. For more information, see [Compare financial baselines of a demand](../task/compare-baselines-of-demand.md).

-   **[Select demand currency preference](../task/select-demand-currency.md)**  
Set your currency preference to use for managing and tracking the financials of your demands from the functional currency, regional currency, or local currency.
-   **[Enable demand currency view](../task/enable-multicurrency-demand.md)**  
Switch to the demand currency view to track the planned costs of a demand in the selected currency.
-   **[Quick start tests for Multicurrency in Demand Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-ppm-demand-multicurrency.md)**  
Validate that the multicurrency in Demand Management still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Upgrade existing demands](../task/upgrade-demand-demand-currency.md)**  
Execute scheduled jobs to upgrade your existing active and inactive demands, respectively, after activating the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

**Parent Topic:**[Configuring Demand Management](configuring-demand-management.md)

