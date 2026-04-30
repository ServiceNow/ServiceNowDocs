---
title: Install Lead-to-Cash Process Management
description: You can install the Lead-to-Cash Process Management application \(app-l2c-cockpit\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Lead-to-Cash Process Management, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Install Lead-to-Cash Process Management

You can install the Lead-to-Cash Process Management application \(app-l2c-cockpit\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Lead-to-Cash Process Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/05dc7eacff202210aa95ffffffffff1b) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Lead-to-Cash Process Management:

-   Roles
-   Tables
-   Properties

For more information, see [Components installed with Lead-to-Cash Process Management](../reference/components-installed-lead-cash-process-management.md) and [Properties installed with Lead-to-Cash Process Management](../reference/properties-installed-lead-cash-process-management.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Lead-to-Cash Process Management application \(app-l2c-cockpit\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you is displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## Result

The Lead-to-Cash Process Management application is installed on your instance. The Business Object Core application is auto-installed as a dependency. For more information, see [Components installed with Business Object Core](../reference/components-installed-business-object-core.md).

The O2C Objects business object group also becomes available. It contains entities involved in the opportunity-to-cash process, such as opportunity, quote, and order. You can use this group provided you have Opportunity Management, Quote Management, and Order Management apps installed on your ServiceNow instance.

## What to do next

Assign roles to Lead-to-Cash Process Management users so that they can access features and perform tasks using this app. For more information, see [Assign roles to Lead-to-Cash Process Management users](assign-roles-lead-cash-process-management.md).

