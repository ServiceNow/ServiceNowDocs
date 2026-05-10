---
title: Install ITOM SU Licensing
description: Install or update the ServiceNow ITOM SU Licensing \[sn\_itom\_licensing\] to ensure you use the latest licensing functionality. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Operational Technology Management licensing and subscriptions, Operational Technology]
---

# Install ITOM SU Licensing

Install or update the ServiceNow® ITOM SU Licensing \[sn\_itom\_licensing\] to ensure you use the latest licensing functionality. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [ITOM SU Licensing](https://store.servicenow.com/sn_appstore_store.do#!/store/application/4cce117e53b9301046dfddeeff7b12eb) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

Prior to Q1 2022, the original licensing mechanism was delivered as part of the family releases. Since then the licensing mechanism is delivered using ServiceNow® ITOM SU Licensing on ServiceNow Store. The system automatically installs ServiceNow® ITOM SU Licensing. You receive notifications when updates for this application are available on ServiceNow Store.

The following items are installed with ITOM SU Licensing:

-   Scheduled jobs
-   Tables

For more information, see [Components installed with ITOM SU Licensing for OTM](../../it-operations-management/reference/components-installed-otm-su-licensing.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application \(sn\_itom\_licensing\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Update** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Update**.

    In the Install dialog that is displayed, any dependencies that are installed along with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Update**.


