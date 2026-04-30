---
title: Install Cloud Cost Management
description: You can install the Cloud Cost Management application \(sn\_clin\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Install Cloud Cost Management

You can install the Cloud Cost Management application \(sn\_clin\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Cloud Cost Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8d562e6253131300f521ddeeff7b125d/) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Discovery \(com.snc.discovery\) and Discovery and Service Mapping Patterns \(sn\_itom\_pattern\) must be installed.

Role required: admin

## About this task

The following items are installed with Cloud Cost Management:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Cloud Cost Management](../reference/installed-with-ci.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Cost Management application \(sn\_clin\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

    **Important:**

    -   If you don't load the demo data during installation, it's unavailable to load later.
    -   If you install demo data, Cloud Cost Management features might not work properly.
6.  Select **Install**.


