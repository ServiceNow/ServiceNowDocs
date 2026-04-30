---
title: Install CMDB success advisor
description: You can install the CMDB success advisor application \(sn\_cmdb\_advisor\) if you have the admin role. The application installs related ServiceNow applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Install CMDB success advisor

You can install the CMDB success advisor application \(sn\_cmdb\_advisor\) if you have the admin role. The application installs related ServiceNow applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Make sure that you have the required entitlements and that all dependent applications are installed on your instance.
-   Review the [CMDB success advisor](https://store.servicenow.com/store/app/db28ec5b87bba254221e8409dabb355c) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with CMDB success advisor:

-   Scheduled jobs
-   Tables

For more information, see [Components installed with CMDB success advisor](../reference/cmdb-sa-components-installed.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the CMDB success advisor application \(sn\_cmdb\_advisor\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


