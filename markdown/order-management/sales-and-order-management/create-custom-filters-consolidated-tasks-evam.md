---
title: Customize Tasks tab views using EVAM
description: Customize the sales entities from which the tasks are displayed, icon and fields that are displayed on each task tile, and create custom options to filter and view consolidated tasks on the sales process dashboard in Lead-to-Cash Process Management using Entity View Action Mapping \(EVAM\).
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customizing the sales process dashboard, Lead-to-Cash Process Management, Order operations apps, Configure, Sales and Order Management]
---

# Customize Tasks tab views using EVAM

Customize the sales entities from which the tasks are displayed, icon and fields that are displayed on each task tile, and create custom options to filter and view consolidated tasks on the sales process dashboard in Lead-to-Cash Process Management using Entity View Action Mapping \(EVAM\).

## Before you begin

Role required: admin or evam\_admin

## About this task

**Note:** Use SPR task EVAM definition for customizing Tasks tab views. Custom EVAM definitions are not supported.

## Procedure

1.  Log in to your ServiceNow instance.

2.  Select the Globe icon ![](../../../reuse/icons/product-icons/globe-outline-24.svg) and set the application scope to Lead-to-Cash Process Management.

3.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **EVAM Definitions**.

4.  In the **Name** column, search for and select SPR task.

5.  In the **EVAM Datasource M2Ms** tab, add or remove a data source.

    -   Create and Link: Define a new data source and then link this data source to your EVAM definition. For more information, see [Define a data source](https://www.servicenow.com/docs/access?context=define-evam-datasource&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

        **Note:** When specifying a condition to define how the data is filtered from the selected table, select the operator as **is not empty** for the business entity you're adding. For example, **\[Quote\]\[is not empty\]**.

    -   Link Existing: Add a predefined data source to your EVAM definition.
    -   Unlink Selected: Unlink a data source you don't want to see on the Tasks tab in the sales process dashboard.
6.  Select **Submit**.

7.  In the **EVAM View Config Bundle M2Ms** tab, add or remove a configuration bundle.

    -   Create and Link: Define a new configuration bundle and then link this bundle to your EVAM definition. For more information, see [Defining an EVAM configuration bundle](https://www.servicenow.com/docs/access?context=define-view-configuration-bundle&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Defining an EVAM view template](https://www.servicenow.com/docs/access?context=define-evam-template&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
    -   Link Existing: Add a predefined configuration bundle to your EVAM definition.
    -   Unlink Selected: Remove the view config bundle for entities you don't want to display.
8.  Add more data filter options on the Tasks tab of the sales process dashboard.

    1.  In the EVAM Data Filters related list, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Label name of the EVAM data filter.|
        |Active|Option to activate the EVAM data filter.|
        |Order|Priority for the EVAM view configuration. Lower numbers indicate a higher priority.|
        |Application|Application scope of the EVAM view configuration.|
        |EVAM Definition|Associate an EVAM definition with the data filter.|

9.  Select **Submit**.


**Parent Topic:**[Customizing the sales process dashboard](../concept/customizing-sales-process-dashboard.md)

**Related topics**  


[Create an EVAM definition](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

