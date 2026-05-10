---
title: Install Robotic Process Automation \(RPA\) Hub
description: You can install the Robotic Process Automation \(RPA\) Hub application \(sn\_rpa\_fdn\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Getting started, RPA Hub, Workflow Data Fabric]
---

# Install Robotic Process Automation \(RPA\) Hub

You can install the Robotic Process Automation \(RPA\) Hub application \(sn\_rpa\_fdn\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [RPA Hub](https://store.servicenow.com/sn_appstore_store.do#!/store/application/7a842080c3103010c573d833a840dd36/2.0.6?referer=/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem%253Butility%253Btemplate&q=RPA&sl=sh) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Robotic Process Automation \(RPA\) Hub:

-   Roles
-   Scheduled jobs
-   Tables
-   Actions and subflow

For more information, see [Components installed with RPA Hub](../../rpa-hub/reference/installed-with-rpa-hub.md) and [Workflow Studio actions and subflow in RPA Hub](../../rpa-hub/reference/rpa-hub-actions.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Robotic Process Automation \(RPA\) Hub application \(sn\_rpa\_fdn\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Robotic Process Automation \(RPA\) Hub.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

Use the Robotic Process Automation \(RPA\) Guided Setup to configure the application on your instance.

To access Robotic Process Automation \(RPA\) Guided Setup, navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md).

