---
title: View license report for the IT Asset Management application
description: IT Asset Management \(ITAM\) applications discover, monitor, and provision resources that are stored in the CMDB as configuration items \(CIs\). The ITAM licensing module combines this CI information with your organization’s purchased subscription data to show subscription usage by application. This helps you confirm that your subscription usage aligns with what your organization purchased, so you can avoid under-licensing or overspending.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/view-itam-license-sum.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Subscriptions for Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# View license report for the IT Asset Management application

IT Asset Management \(ITAM\) applications discover, monitor, and provision resources that are stored in the CMDB as configuration items \(CIs\). The ITAM licensing module combines this CI information with your organization’s purchased subscription data to show subscription usage by application. This helps you confirm that your subscription usage aligns with what your organization purchased, so you can avoid under-licensing or overspending.

## Before you begin

Role required: usage\_admin, admin.

## About this task

The following interactions collect and aggregate the information used for licensing. As a result, you can view statistics on how your organization uses purchased subscription units.

1.  The IT Asset Management applications count CIs and assign them to CI categories each day.
2.  The IT Asset Management applications report CI counts by CI category to the licensing module each day. If features of the same application report the same CIs as their resources, the CI count is adjusted to remove the duplication.
3.  The licensing module correlates the daily average CI counts for IT Asset Management applications with the licensing information from the customer contract to produce license statistics.

## Procedure

1.  Navigate to **All** &gt; **ITAM Licensing** &gt; **ITAM License Report**.

2.  Select an application to view the subscription for a particular CI category.

    \[Omitted image "itam-licensing-report.png"\] Alt text: ITAM license summary

    You can view the following information on CI count and subscriptions purchased for each IT Asset Management application separately \(a la carte\).

    |Metric|Description|
    |------|-----------|
    |Resource Category|CI categories for IT Asset Management applications.|
    |Resource Total Count|CI count organized by CI category, for each IT Asset Management application.|
    |Subscription Unit Ratio|Ratios show the subscription units to managed IT resources, in the form subscription units:resource. The Software Asset Management application has pre-defined values for End User Computing Devices \(1:4\), Servers \(1:1\), IaaS storage \(1:3\), PaaS resources \(1:3\), and SaaS subscription users \(1:15\).|
    |Total Subscription Units Consumed|Number of subscriptions consumed per CI category, for each IT Asset Management application. The licensing module calculates this number by applying the subscription ratio to the CI count for each application's CI category.|

    For licensing purposes, Software Asset Management counts only CIs with software installs that were discovered within the last 90 days or the last discovered date is empty

    CIs are also excluded if a custom column is added to the cmdb\_ci\_hardware table and that column is referenced in the **Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Management** property.

    For more information about excluding CIs, see [Exclude software assets on CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/exclude-software-assets-cis.md).


**Parent Topic:**[Subscriptions for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-subscription.md)

