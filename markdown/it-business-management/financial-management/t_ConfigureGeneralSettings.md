---
title: Configure general settings
description: Configure the level of detail for allocation lines on the Configuration tab of the workbench.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [The Configuration tab, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure general settings

Configure the level of detail for allocation lines on the **Configuration** tab of the workbench.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## About this task

You can vary the level of detail that is available on allocation data. The application can keep track of Sys\_IDs of segment values in the allocation line tables, which allows you to dot-walk on allocation reports. This might have a performance impact on your application, depending on the number of allocation lines you generate.

## Procedure

1.  On the workbench, click the **Configuration** tab.

    The currency code for the base system currency is shown in the **General Settings** pane.

    **Note:**

    Until Kingston release, you can use **com.glide.financial\_management.currency\_code** property to get the currency code. The property was removed in London release. If you are an upgraded customer in London, you can still use this property. Currently, **glide.system.locale** is the functional currency.

    To get the currency code, use the new scriptable SNC.FMCurrency\(\).getGlobalCurrencyCode\(\) API irrespective of you being an upgraded or a new customer.

2.  Enable the **Basic Allocation Setup** to open the allocation setup UI in a lighter mode.

    **Note:** If you are a non-analyst licensed customer, the option is enabled automatically if the number of accounts in a segment or the total number of accounts in the cost model exceeds the threshold values 4000 and 12000 respectively.

3.  Enable **Missing Money Analysis** to enable the log in the Allocation Setup page of the Workbench.

    Missing money analysis is an extended and improved version of the allocation log functionality that was available before the Madrid release.

4.  **Display Records per segment** is a configuration setup that helps you to choose the number of accounts such as 5, 10, 15, 25, or 50 of a segment for display in the Allocation Setup page of the workbench, Allocation Setup page of lighter workbench, and the Cost Lines Analysis page.


**Parent Topic:**[The Configuration tab](../concept/c_TheConfigurationTab.md)

**Related topics**  


[Configure main report settings](t_ConfigureMainReportSettings.md)

[Delete allocation lines](t_DeleteAllocationLines.md)

