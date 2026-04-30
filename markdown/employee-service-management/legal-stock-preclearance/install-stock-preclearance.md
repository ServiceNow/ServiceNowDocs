---
title: Install Legal Stock Preclearance
description: You can install the Legal Stock Preclearance application \(sn\_lg\_stock\_cp\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: zurich
product: Legal Stock Preclearance
classification: legal-stock-preclearance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Stock Preclearance, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Install Legal Stock Preclearance

You can install the Legal Stock Preclearance application \(sn\_lg\_stock\_cp\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

**Note:**

The Legal Stock Preclearance application is installed automatically when you install the Legal Simple Compliance suite.

-   Verify that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Legal Stock Preclearance](https://store.servicenow.com/sn_appstore_store.do#!/store/application/523a117673da2300844489b954f6a7d6) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following components are installed with installation of the Legal Stock Preclearance application:

-   Plugins
-   Store applications
-   Roles
-   Tables
-   Business Rules

For more information, see [Components installed with Legal Stock Preclearance](../reference/installed-with-legal-stock-preclearance.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Legal Stock Preclearance application \(sn\_lg\_stock\_cp\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed that are already installed, will be installed, or must be installed. If any plugins or applications need to be installed, you must install them before you can install Legal Stock Preclearance.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

Use the Legal Service Delivery Guided Setup to configure the application on your instance.

To access Legal Service Delivery Guided Setup, navigate to **Legal Administration** &gt; **Legal Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Configure Legal Stock Preclearance](../concept/legal-stock-pre-administration.md)

