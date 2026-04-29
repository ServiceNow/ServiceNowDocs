---
title: Install Customer Project Management
description: You can install the Customer Project Management application \(com.snc.csm\_ppm\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with Customer Project Management, Integrate, Customer Service Management]
---

# Install Customer Project Management

You can install the Customer Project Management application \(com.snc.csm\_ppm\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

This plugin requires the Customer Service plugin \(com.sn\_customerservice\) and the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

The Customer Project Management application adds the **Customer Service** &gt; **Projects** module to the application navigator. Users with the customer project manager role can access this module.

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Customer Project Management application listing](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ca994c6287723300f734a7da0acb0b41/2.0.0) in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Customer Project Management application \(com.snc.csm\_ppm\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


