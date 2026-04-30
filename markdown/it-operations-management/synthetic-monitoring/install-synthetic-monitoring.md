---
title: Install synthetic monitoring
description: You can install the synthetic monitoring application \(com.snc.uib.sow\_synthetics\) with the admin role.
locale: en-US
release: zurich
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Install synthetic monitoring

You can install the synthetic monitoring application \(`com.snc.uib.sow_synthetics`\) with the admin role.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [synthetic monitoring](https://store.servicenow.com/sn_appstore_store.do#!/store/application/16ade75aa323021035ce4514d31e61aa/1.0.0) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Confirm that the Configuration items \(CI\) that you want to monitor exist in the CMDB HTTP Endpoints \[cmdb\_ci\_endpoint\_http\] table.
-   Confirm that configured credentials exist in the Credentials \[discovery\_credentials\] table if your endpoint requires authentication.

    **Note:** Synthetic monitoring supports API key credentials, basic authentication credentials, and OAuth.


Role required: sn\_sow\_synthetics.synthetics\_admin

## About this task

The following items are installed with synthetic monitoring:

-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with synthetic monitoring](../reference/components-installed-with-synthetic-monitoring.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the synthetic monitoring application \(com.snc.uib.sow\_synthetics\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## What to do next

[Create synthetic monitoring locations](create-synthetic-monitoring-locations.md)

**Parent Topic:**[Configuring synthetic monitoring](../concept/configuring-synthetic-monitoring.md)

