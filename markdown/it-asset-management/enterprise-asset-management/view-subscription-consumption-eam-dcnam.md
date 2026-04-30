---
title: View your subscription consumption for the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application
description: Use the ITAM Licensing Resource Counts \[itam\_licensing\_resource\_counts\] table to gain insight into your subscription consumption for the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\), Enterprise Asset Management, IT Asset Management]
---

# View your subscription consumption for the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application

Use the ITAM Licensing Resource Counts \[itam\_licensing\_resource\_counts\] table to gain insight into your subscription consumption for the Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) application.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

The EAM Populate Licensing Data scheduled job runs every Sunday to generate subscription consumption information for the application. Any changes to your subscription consumption are reflected only after the weekly scheduled job runs.

## Procedure

1.  On the page header of your ServiceNow instance, select **All**.

2.  In the menu navigation filter, enter `itam_licensing_resource_counts_list.do`.

    The ITAM Licensing Resource Counts \[itam\_licensing\_resource\_counts\] table opens.

3.  In the table, locate all entries for the Enterprise Asset Management for DCNAM application.

    ![ITAM Licensing Resource Counts table.](../image/itam-licensing-resource-counts-table.png)

    If the table includes multiple applications, you can locate all entries for the Enterprise Asset Management for DCNAM application by using any of the following options:

    -   If you want to sort the table by application, use the following steps:

        1.  Select the Column options icon ![](../image/configure-options-icon.png)next to the Application column name.

            Alternatively, right-click the Application column name.

        2.  Select an option to sort the applications in either ascending or descending alphabetical order.
            -   To sort the applications in ascending alphabetical order, select **Sort \(a to z\)**.
            -   To sort the applications in descending alphabetical order, select **Sort \(z to a\)**.
        You can then locate all entries for the Enterprise Asset Management for DCNAM application.

    -   If you want to group the table by application, use the following steps:

        1.  Select the Column options icon ![](../image/configure-options-icon.png)next to the Application column name.

            Alternatively, right-click the Application column name.

        2.  Select **Group By Application**.
        You can then expand the **Application: Enterprise Asset Management for DCNAM** group to view all entries for the application.

    -   If you want the table to display only the Enterprise Asset Management for DCNAM application, use the following steps:

        1.  On the table header, set the search filter to **Application**.
        2.  In the corresponding search box, enter `Enterprise Asset Management for DCNAM`.
        3.  Press the Enter key.
        Alternatively, you can right-click the Enterprise Asset Management for DCNAM application name in the table and then select **Show Matching**.

4.  View the following subscription consumption information for the application.

    **Note:** Subscription consumption information is generated and grouped by resource category. For more information on resource categories, see [Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\) licensing](../concept/eam-dcnam-licensing.md).

    |Field|Description|
    |-----|-----------|
    |Application|Name of the application.|
    |Resource Category|Resource category that is supported by the application.|
    |Resource Subcategory|Subcategory of the given resource category.|
    |Resource Total Count|Total number of assets within the given resource category and subcategory.|
    |Subscription Unit Ratio|Predefined ratio that indicates how many assets within the given resource category require a subscription. For example, a ratio of 25:1 indicates that one subscription is required for every 25 assets within the resource category.|
    |Total Subscription Units Consumed|Total number of subscriptions that you have consumed for the given resource category and subcategory. The ITAM licensing module calculates this value by applying the Subscription Unit Ratio to the Resource Total Count.|


**Parent Topic:**[Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](../concept/eam-dcnam.md)

