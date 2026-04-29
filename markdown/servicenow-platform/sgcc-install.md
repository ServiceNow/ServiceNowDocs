---
title: Install SGC Central
description: You can install the SGC Central application \(sn\_sgc\_central\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring SGC Central, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Install SGC Central

You can install the SGC Central application \(sn\_sgc\_central\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [SGC Central](https://store.servicenow.com/sn_appstore_store.do#!/store/application/0327142c93def150b7b532bb5cba10db) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Review the supported CMDB Workspace versions for the corresponding ServiceNow versions as listed in the following table.

<table id="table_qbn_cny_wcc"><thead><tr><th>

ServiceNow versions

</th><th>

Supported CMDB Workspace versions

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

8.0.0 or later

</td></tr><tr><td>

Zurich

</td><td>

7.4.1 or later

</td></tr><tr><td>

Yokohama

</td><td>

7.3.0 or later

</td></tr></tbody>
</table>
Role required: admin

## About this task

The following items are installed with SGC Central:

-   Plugins
-   Store applications
-   Scheduled jobs
-   Tables

For more information, see [Components installed with SGC Central](../concept/sgcc-installed-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the SGC Central application \(sn\_sgc\_central\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


