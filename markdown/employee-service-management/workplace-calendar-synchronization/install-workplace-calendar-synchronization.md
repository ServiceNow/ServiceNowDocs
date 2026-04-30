---
title: Install Workplace Calendar Synchronization
description: Install the Workplace Calendar Synchronization application from ServiceNow Store applications. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Calendar Synchronization

Install the Workplace Calendar Synchronization application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup instructions to view the available subscriptions:

Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.

Use the following details when required:

-   Name of the application: Workplace Calendar Synchronization
-   ID of the application: sn\_wsd\_rsvsync

Role required: admin

## About this task

The following plugins are activated when you install Workplace Calendar Synchronization:

-   Workplace Core \(sn\_wsd\_core\) minimum version 2.3.3
-   Workplace Reservation Management \(sn\_wsd\_rsv\) minimum version 1.3.3
-   -   Depending on the calendar provider that you want to configure, instal the following plugins:

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Calendar Synchronization\) or ID \(sn\_wsd\_rsvsync\). If you cannot find the application, you may have to request it from the ServiceNow Store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Calendar Synchronization.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Calendar Synchronization](../concept/configure-rsv-sync.md)

**Related topics**  


[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

