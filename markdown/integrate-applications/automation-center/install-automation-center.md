---
title: Install Automation Center
description: If you have the admin role, you can install the Automation Center application \(sn\_ac\). If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Automation Center, Workflow Data Fabric]
---

# Install Automation Center

If you have the admin role, you can install the Automation Center application \(sn\_ac\). The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Automation Center](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ae2a30de771001100175a9077b5a999e) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Automation Center:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Automation Center](../reference/components-installed-with-automation-center.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Automation Center application \(sn\_ac\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

The data in Automation Center Value dashboard is derived from the Performance Analytics \(PA\) tables. The PA jobs are scheduled to run at a specific time in the day. If you want to view the data immediately after the installation and before the scheduled run, then you have to manually run the PA jobs.

**Parent Topic:**[Configuring Automation Center](../concept/automation-center-setup.md)

