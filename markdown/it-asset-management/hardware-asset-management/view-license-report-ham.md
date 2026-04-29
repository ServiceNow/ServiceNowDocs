---
title: View the license report for the Hardware Asset Management application
description: View details of the subscriptions purchased and consumed by your organization for the managed IT resource types such as Server, End User Computing Device, Networking Device, Mobile Device, and Telecom Network Inventory using the ITAM License Report.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [HAM licensing, Hardware Asset Management licensing]
breadcrumb: [Manage Hardware Asset Management subscriptions, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# View the license report for the Hardware Asset Management application

View details of the subscriptions purchased and consumed by your organization for the managed IT resource types such as Server, End User Computing Device, Networking Device, Mobile Device, and Telecom Network Inventory using the ITAM License Report.

## Before you begin

Role required: admin, usage\_admin

## About this task

**Note:** Every week on Sunday, the license count for the managed IT resource types is calculated. Any changes to the license consumption reflect on the ITAM license report only after the weekly license count calculation.

## Procedure

1.  Navigate to **All** &gt; **ITAM Licensing** &gt; **ITAM License Report**.

2.  Search for the Hardware Asset Management application.

    ![ITAM License Report](../image/itam-license-ham.png)

    Subscription details of all the Hardware Asset Management applications activated on your ServiceNow instance are shown.

    You can view the following information on subscriptions purchased for the resource categories that you opted-in for allthe Hardware Asset Management applications:

    -   **Application**: Name of the application that is activated on your ServiceNow instance. The ITAM License Report is grouped by the application.
    -   **Resource Category**: Managed IT resource types available for the Hardware Asset Management application. The resource types include the following:

        -   Server
        -   End User Computers
        -   Network gear
        -   Mobile Device
        -   Telecom Network Inventory
        -   Printers
        -   Monitors
        -   Storage
        -   Unclassified hardware
        Note the following:

        -   Printers, Monitors, Storage, and Unclassified hardware are available with Hardware Asset Management version 10.1.0 and later.
        -   When more than one Hardware Asset Management solution is activated on your ServiceNow instance, an opted-in resource category that is available with the activated solutions is licensed only under solution. For more details, see [Licensing framework for Hardware Asset Management solutions](../concept/licensing-ham-solutions.md).
    -   **Resource Subcategory**: Subcategories of a Resource category.

        **Note:**

        -   Resource Subcategory is available with Hardware Asset Management version 10.1.0 and later.
        -   Based on the acquisition method, the following resource subcategories are available for the Mobile Device only when the Hardware Asset Management integration with Zero Touch Mobility is activated on your ServiceNow instance:
            -   Bring Your Own Asset
            -   Corporate Asset
    -   **Resource Total Count**: Asset count of the managed IT resources that is grouped by Resource categories and Model categories.
    -   **Subscription Unit Ratio**: Predefined ratios that determine how many assets of a Resource category require a subscription. For example, the defined ratio of 4:1 for End User Computers means that every four assets of that resource category require one Subscription Unit.
    -   **Total Subscription Units Consumed**: The number of subscriptions per Resource category that your organization consumed. The licensing module calculates this number by applying the Subscription Unit Ratio to the Resource Total Count for each Resource Category.

**Parent Topic:**[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

**Related topics**  


[Opt-in or opt-out of HAM license resource categories](optin-optout-ham-license-resource-categories.md)

[Exclude assets](exclude-assets.md)

