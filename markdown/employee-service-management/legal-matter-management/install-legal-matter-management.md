---
title: Install Legal Matter Management
description: You can install the Legal Matter Management application \(sn\_lg\_matter\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Legal Matter Management, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Install Legal Matter Management

You can install the Legal Matter Management application \(sn\_lg\_matter\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If the application requires plugins or other store applications, install them first if they are not already installed.
-   Review the [Legal Matter Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8570d70bb32313007a6de81816a8dcf3) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following components are installed with installation of the Legal Matter Management application:

-   Plugins
-   Store applications
-   Roles
-   Tables
-   Tables specific to practice areas
-   Business Rules

See [Components installed with Legal Matter Management](../reference/installed-with-legal-matter-management.md) for more information.

You can also install the following applications:

-   **Legal Counsel Center application \(sn\_lg\_cf\_workspace\)**

    The ServiceNow® Legal Counsel Center application enables lawyers to solve issues faster with a workspace built to facilitate resolutions. From a single view, get the full context of legal issues to resolve them quickly.

-   **Legal Counsel Center Components \(sn\_lg\_ws\_comps\)**

    The ServiceNow® Legal Counsel Center Components application enhances the workspace experience for the Legal Counsel Center by decoupling the components in the Legal Counsel Center to offer better performance.

-   **Legal Mobile \(sn\_lg\_mobile\)**

    The ServiceNow® Legal Mobile \(sn\_lg\_mobile\) application enables you to find legal information, submit and track legal requests, and work on these requests on mobile devices. For more information, see [Legal Mobile](../../legal-mobile/concept/legal-mobile-overview.md).


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Legal Matter Management application \(sn\_lg\_matter\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Legal Matter Management.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

Use the Legal Service Delivery Guided Setup to configure the application on your instance.

To access Legal Service Delivery Guided Setup, navigate to **Legal Administration** &gt; **Legal Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Setting up Legal Matter Management](../concept/setting-up-legal-matter-managemment.md)

