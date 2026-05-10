---
title: View license report for the IT Asset Management application
description: Resources that the IT Asset Management applications discover, monitor, and provision are configuration items \(CIs\) stored in the CMDB. The ITAM licensing module combines this information on CIs with the information on subscriptions your organization purchased to produce statistics on subscription use by IT Asset Management applications.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Subscriptions for Software Asset Management, Software Asset Management, IT Asset Management]
---

# View license report for the IT Asset Management application

Resources that the IT Asset Management applications discover, monitor, and provision are configuration items \(CIs\) stored in the CMDB. The ITAM licensing module combines this information on CIs with the information on subscriptions your organization purchased to produce statistics on subscription use by IT Asset Management applications.

## Before you begin

The process of collecting and aggregating information for licensing purposes consists of the following interactions. As a result, you can view the statistics on how your organization uses purchased subscription units.

1.  The IT Asset Management applications count CIs and assign them to CI categories daily.
2.  The IT Asset Management applications daily report CI count by CI category to the IT Asset Management licensing module. If features of the same application report the same CIs as their resources, the CI count is manipulated to remove the duplication.
3.  The licensing module correlates the daily average CI counts for IT Asset Management applications with the licensing information from the customer contract to produce license statistics.

Role required: usage\_admin

## Procedure

1.  Navigate to **All** &gt; **ITAM Licensing** &gt; **ITAM License Report**.

2.  Select an application to view the subscription for a particular CI category.

    ![ITAM license summary](../image/itam-licensing-report.png)

    You can view the following information on CI count and subscriptions purchased for each IT Asset Management application separately \(a la carte\):

    -   **Resource Category**: CI categories for IT Asset Management applications.
    -   **Resource Total Count**: CI count for CIs organized by CI categories, for each IT Asset Management application.
    -   **Subscription Unit Ratio**: Ratios define how many CIs of a certain CI category require a subscription. The Software Asset Management application has pre-defined values for End User Computers \(4:1\), for Servers \(1:1\), for Storage Volumes \(3:1\), for Databases \(3:1\), and for Subscription Users \(15:1\).
    -   **Total Subscription Units Consumed**: The number of subscriptions per CI category for each IT Asset Management application that your organization consumed. The licensing module calculates this number by applying the subscriptions ratio to the CI count number for each application's CI category.
    For licensing purposes, the Software Asset Management application only considers CIs with software installs discovered within the last 90 days or those where the last discovered as empty. Additionally, all CIs are excluded that have a column added to the cmdb\_ci\_hardware table and that column name is referenced in the property labeled **Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Management**. For more information on excluding CIs, see [Exclude software assets on CIs](../../software-asset-management2/task/exclude-software-assets-cis.md).


**Parent Topic:**[Subscriptions for Software Asset Management](../../software-asset-management2/concept/sam-subscription.md)

