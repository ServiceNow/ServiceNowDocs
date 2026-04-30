---
title: Install Cloud Cost Management Infra Stack
description: You can install the Cloud Cost Management Infra Stack application \(sn\_cld\_infra\_stack\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Install Cloud Cost Management Infra Stack

You can install the Cloud Cost Management Infra Stack application \(sn\_cld\_infra\_stack\) if you have the admin role.The application includes installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Cloud Cost Management Infra Stack application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Cloud Cost Management Infra Stack:

-   Plugins
-   Store applications

The tables, scheduled jobs, and system properties aren't installed with the Cloud Cost Management Infra Stack application. Instead, the components specific to Cloud Cost Management Infra Stack are installed with the Cloud Cost Management application. For more information, see [Components installed with Cloud Cost Management](../reference/installed-with-ci.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Cost Management Infra Stack application \(sn\_cld\_infra\_stack\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


