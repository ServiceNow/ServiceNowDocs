---
title: Check which CI types require an ITOM subscription
description: View the list of configuration item \(CI\) types that require IT Operations Management subscription units.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Check which CI types require an ITOM subscription

View the list of configuration item \(CI\) types that require IT Operations Management subscription units.

## Before you begin

Ensure that your organization has purchased ITOM subscriptions. You cannot view the information in the **ITOM License** module without subscriptions.

Role required: sn\_itom\_license.reader

## About this task

For licensing purposes, licensable resources are assigned to CI categories. License usage is measured using subscription units, which may cover a different number of resources, depending on the resource CI category. The customer contract for your organization determines the CI categories from the available options, and also the ratios of CI allocation for subscription units in each CI category. Information from the customer contract is synchronized with the ServiceNow platform. The latest version of ServiceNow® ITOM/OT SU Licensing supports the following CI categories:

-   Containers
-   PaaS
-   FaaS
-   Servers
-   Unresolved Monitored Object
-   Unclassed category
-   End User Devices
-   IoT
-   Customer Prem Devices

The system stores information about CI categories and CI types that belong to them in the ITOM Licensing MetaData \[itom\_lu\_metadata\] table. This table includes information only about parent CI types. All CI types that are created by extending these parent CI types are included by default. For example, the Apache Web Server CI type is included in the CI count, because it is an extension of the Web Server CI type.

## Procedure

1.  Check which CI category is licensable:

    1.  Navigate to **All** &gt; **ITOM License** &gt; **License Summary**.

    2.  Select the relevant ITOM subscription.

        For example, **ITOM Visibility**.

    3.  Scroll down and select the **ITOM CI subscription unit ratio** tab.

        The tab lists licensable CI categories generated from the customer contract. These are the licensable CI categories.

    4.  Make a note of the licensable CI categories provided for this ITOM subscription.

    5.  Return to the **License Summary** list and check CI categories generated for other ITOM subscriptions.

2.  Navigate to **All** &gt; **ITOM License** &gt; **Licenses by CI Type**.

    **Important:** The ITOM Licensing MetaData \[itom\_lu\_metadata\] table contains all CI categories, including categories of CIs that do not require ITOM subscription units.

3.  Review the list to identify licensable CI categories that appear on the **ITOM CI subscription unit ratio** tab of the **License Summary** list.

    The customer contract for your organization determines the ratios of CI allocation for subscription units in each CI category, and this information is synchronized with the ServiceNow platform.

4.  Select the arrow adjacent to the licensable CI category to expand it and access the associated CI types.

    The CI types listed under CI categories require ITOM subscription units for access.


