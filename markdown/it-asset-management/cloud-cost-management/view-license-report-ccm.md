---
title: View the license report for the Cloud Cost Management application
description: View details of the subscriptions purchased and consumed by your organization for the managed IT resource types such as Server, End User Computing Device, and Database using the ITAM License Report.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-17"
reading_time_minutes: 1
breadcrumb: [Manage Cloud Cost Management subscriptions, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# View the license report for the Cloud Cost Management application

View details of the subscriptions purchased and consumed by your organization for the managed IT resource types such as Server, End User Computing Device, and Database using the ITAM License Report.

## Before you begin

Role required: admin, usage\_admin

## Procedure

1.  Navigate to **All** &gt; **ITAM Licensing** &gt; **ITAM License Report**.

2.  Select the Software Asset Management application to view the subscription for Cloud Cost Management.

    Subscription details of all the Cloud Cost Management applications activated on your ServiceNow instance are shown.

    ![License report for Cloud Cost Management](../image/ccm-subscriptions.png)

    You can view the following information on subscriptions purchased for the resource categories that you opted-in for the Cloud Cost Management application:

    -   **Application**: Name of the application that is activated on your ServiceNow instance. The ITAM License Report is grouped by the application.
    -   **Resource Category**: Managed IT resource types available for the Cloud Cost Management application. The resource types include the following:
        -   Server
        -   Virtual machines
        -   Databases
        -   Storage volumes
    -   **Resource Total Count**: Asset count of the managed IT resources that is grouped by Resource categories and Model categories.

        The Cloud License Estimator enables you to determine the estimated resource count for all the cloud resources that are eligible for licensing based on Cloud Cost Management licensing rules. For more information, see [Cloud License Estimator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-license-estimator/explore-cloud-license-estimator.md).

    -   **Subscription Unit Ratio**: Predefined ratios that determine how many assets of a Resource category require a subscription. For example, the defined ratio of 1:1 for Server means that every asset of that resource category requires one Subscription Unit.
    -   **Total Subscription Units Consumed**: The number of subscriptions per Resource category that your organization consumed. The licensing module calculates this number by applying the Subscription Unit Ratio to the Resource Total Count for each Resource Category.

**Parent Topic:**[Manage Cloud Cost Management subscriptions](../concept/managing-ccm-subscriptions.md)

