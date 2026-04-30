---
title: Install Critical Event Management
description: You can install the Critical Event Management application with the admin role. If the demo data and related applications aren’t installed by default, the application includes demo data to install them.
locale: en-US
release: yokohama
product: Critical Event Management
classification: critical-event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Critical Event Management, Health and Safety, Employee Service Management]
---

# Install Critical Event Management

You can install the Critical Event Management application with the admin role. If the demo data and related applications aren’t installed by default, the application includes demo data to install them.

## Before you begin

-   Verify that the application and all of its associated applications have valid entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Critical Event Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/480eafd51b8682906f32b8449b4bcbc6) application listing in the ServiceNow® Store for information on dependencies, licensing, or subscription requirements.

Role required: admin

## About this task

The following items are installed with Critical Event Management:

-   Plugins
-   Store Applications
-   Roles
-   Tables

For more information, see [Components installed with Critical Event Management](../reference/components-installed-with-cem.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Critical Event Management application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

3.  Select a version from the list and select **Install**.

    In the Install dialog box that is displayed, any dependencies that are installed along with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Select **Install**.


