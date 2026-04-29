---
title: View the license report for the OT Asset Management application
description: View details of the subscriptions consumed by your organization for the OT Asset Management application by using the ITAM License Report.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OT Asset Management licensing, OT Asset Management, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# View the license report for the OT Asset Management application

View details of the subscriptions consumed by your organization for the OT Asset Management application by using the ITAM License Report.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

The EAM Populate Licensing Data job runs every Sunday and populates the ITAM License Report. Any changes to the license consumption will reflect on the ITAM license report only after the weekly license count calculation.

## Procedure

1.  Navigate to **All** &gt; **ITAM Licensing** &gt; **ITAM License Report**.

2.  Search for the OT Asset Management application.

    ![ITAM License Report](../image/otam-license-report.png)

    You can view the following information on subscriptions consumed for the resource categories for the OT Asset Management application.

    -   **Application**: Name of the application that is activated on your ServiceNow instance. The ITAM License Report can be grouped by the application.
    -   **Resource Category**: Managed OT resource types available for the OT Asset Management application. The resource types include the following:
        -   Unclassed OT
        -   OT Supervisory System
        -   OT Control System
        -   OT Field Devices
        -   Industrial Consumable
        -   Operational Equipment
        -   OT Servers
        -   OT Network Gear
        -   OT Storage
        -   OT End User Computers
        -   OT Mobile Devices
        -   OT Monitors
        -   OT Printers
        -   OT Unclassified Hardware
    -   **Resource Subcategory**: Subcategories of a Resource category.
    -   **Resource Total Count**: Asset count of the managed OT resources that is grouped by Resource categories and Model categories.
    -   **Subscription Unit Ratio**: Predefined ratios that determine how many assets of a Resource category require a subscription. For example, the defined ratio of 25:1 for Industrial Consumable means that every 25 assets of that resource category require one Subscription Unit.
    -   **Total Subscription Units Consumed**: The number of subscriptions per Resource category that your organization consumed. The licensing module calculates this number by applying the Subscription Unit Ratio to the Resource Total Count for each Resource Category.

**Parent Topic:**[OT Asset Management licensing](../concept/licensing-ot-asset-management.md)

