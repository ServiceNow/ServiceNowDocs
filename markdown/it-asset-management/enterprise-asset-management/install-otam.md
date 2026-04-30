---
title: Install OT Asset Management
description: You can install the OT Asset Management application \(com.sn\_otam\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence: The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Enterprise Asset Management by system administrators, Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Install OT Asset Management

You can install the OT Asset Management application \(com.sn\_otam\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: sys\_admin

## About this task

The following items are installed with OT Asset Management:

-   Plugins
-   Store applications
-   Roles

For more information, see [Installed with OT Asset Management](../reference/installed-with-otam.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the OT Asset Management application \(com.sn\_otam\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Enterprise Asset Management by system administrators](../concept/config-eam-sysadmins.md)

