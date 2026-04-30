---
title: Install Event Management
description: Retrieve the most updated apps for the Event Management application \(com.glideapp.itom.snac\) in the ServiceNow Store. Periodically check the ServiceNow Store for new app versions.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Install Event Management

Retrieve the most updated apps for the Event Management application \(com.glideapp.itom.snac\) in the ServiceNow® Store. Periodically check the ServiceNow® Store for new app versions.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Role required: admin

## About this task

The following items are installed with Event Management:

-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Event Management](../reference/r_InstalledWithEventManagement.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ITOM Health application using the filter criteria and search bar.

    If you cannot find the application, request it from the ServiceNow Store.

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Event Management.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.


**Parent Topic:**[Configuring Event Management](../concept/using-event-management.md)

