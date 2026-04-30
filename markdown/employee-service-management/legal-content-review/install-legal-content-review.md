---
title: Install Legal Content Review
description: You can install the Legal Content Review application \(sn\_lg\_cont\_review\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Legal Content Review
classification: legal-content-review
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Content Review, Legal Content Review, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Install Legal Content Review

You can install the Legal Content Review application \(sn\_lg\_cont\_review\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Legal Content Review application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Install the Legal Request Management \(sn\_lg\_ops\) application before you install Legal Content Review.

Role required: sn\_lg\_cont\_review.admin

## About this task

The following items are installed with Legal Content Review:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Legal Content Review application \(sn\_lg\_cont\_review\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

Use the Legal Service Delivery Guided Setup to configure the application on your instance.

To access Legal Service Delivery guided setup, navigate to **Legal Administration** &gt; **Legal Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Setting up Legal Content Review](../concept/setting-up-legal-content-review.md)

