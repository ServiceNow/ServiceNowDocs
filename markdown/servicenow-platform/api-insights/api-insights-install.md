---
title: Install API Insights
description: You can install the API Insights application \(sn\_api\_insights\_ws\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System administrator tasks, Configure, API Insights, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Install API Insights

You can install the API Insights application \(sn\_api\_insights\_ws\) if you have the admin role.The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [API Insights](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8b178af643f37110509fa1fb99b8f285) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with API Insights:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with API Insights](../reference/api-insights-components-installed.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the API Insights application \(sn\_api\_insights\_ws\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


