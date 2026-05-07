---
title: Check CI count used for OTM subscriptions
description: View the daily counts or the averages for the most recent 90 days of CI data. ServiceNow OT Foundation, ServiceNow OT Visibility and ServiceNow OT Vulnerability and Response offer insights into the licensed resources that OTM applications support. Resources that OTM applications discover, monitor, and provision are configuration items \(CIs\) stored in the CMDB. The OTM licensing module combines this CI information with the information on subscriptions your organization purchased to produce statistics on subscription use by OTM applications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Operational Technology Management licensing and subscriptions, Operational Technology]
---

# Check CI count used for OTM subscriptions

View the daily counts or the averages for the most recent 90 days of CI data. ServiceNow OT Foundation, ServiceNow OT Visibility and ServiceNow OT Vulnerability and Response offer insights into the licensed resources that OTM applications support. Resources that OTM applications discover, monitor, and provision are configuration items \(CIs\) stored in the CMDB. The OTM licensing module combines this CI information with the information on subscriptions your organization purchased to produce statistics on subscription use by OTM applications.

## Before you begin

-   Ensure your organization has active OTM subscriptions.
-   Ensure that you installed the latest available version of the ITOM SU Licensing from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/4cce117e53b9301046dfddeeff7b12eb).

Role required: sn\_itom\_license.reader

## About this task

ServiceNow incurs charges for the usage of ServiceNow OT Foundation, ServiceNow OT Visibility and ServiceNow OT Vulnerability and Response. To gain a deeper understanding of the products and features included in OTM subscriptions, see [Subscriptions for OTM](../concept/otm-license-module.md).

The procedure for gathering and consolidating data for licensing purposes involves the following series of actions:

1.  The OTM licensing system calculates the daily count of configuration items \(CIs\) managed by each OTM product, subsequently categorizing these CI counts into distinct licensable CI categories.
2.  In cases where identical configuration items \(CIs\) are being managed by various features within the same OTM products, adjustments are made to eliminate any duplications in the CI count.
3.  In cases where IT configuration items \(IT CIs\) are categorized as OT configuration items, the CIs are counted only once - under OTM licensing and not under ITOM licensing.
4.  The licensing module consolidates CI counts from OTM applications to calculate the average of the daily CI count for the last 90 days.

    **Note:** CIs managed by SG-OT Excel are counted and listed for license consumption with last\_scan dates more recent than, equal to, and older than 90 days ago.

5.  The licensing module matches the daily average CI counts for OTM applications with the licensing details provided in the customer contract to generate license-related statistics.

Consequently, you can view the statistics on how your organization utilizes the purchased subscription units.

View information on CI count and subscriptions purchased for each OTM application separately \(a la carte\):

-   **Total Count**: The average of the CI counts collected over 90 days, categorized by CI types, for each individual OTM application.

    **Note:** CIs managed by SG-OT Excel are counted and listed for license consumption with last\_scan dates more recent than, equal to, and older than 90 days ago.

-   **Subscription Unit Ratio**: Ratios determine how many CIs of a particular CI category necessitate a subscription. The licensing module retrieves this ratio information from customer contracts.
-   **Total Subscription Units Consumed**: The quantity of subscriptions used by your organization for each CI category within each OTM application. This calculation is performed by applying the subscription units ratio to the count of CIs within each respective CI category.
-   **Total Subscription Units Consumed**: The total subscription units consumed by all OTM applications combined.

You can access OTM Subscription Unit \(SU\) consumption categorized by domain. This data can be useful for allocating consumption and expenses to different organizations.

## Procedure

1.  Navigate to **OTM License** &gt; **License Report**.

2.  View the average of daily CI counts for the last 90 days.

3.  To view the daily CI counts, modify the filter to set **Aggregated** to **false**.

    If needed, you can modify the view by sorting the columns. The **Created** column displays the timestamp indicating when the CI information was most recently updated.


