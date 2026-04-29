---
title: Install Workplace Space Management
description: Install the Workplace Space Management application from the ServiceNow Store. Visit the ServiceNow Store to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Space Management

Install the Workplace Space Management application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup instructions:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance.

    The list displays the subscriptions that your organization has purchased.

2.  Verify that the following plugins are activated:
    -   Workplace Core \(sn\_wsd\_core\), minimum version 2.6.2
    -   Workplace Space Management \(sn\_wsd\_spcmgmt\), minimum version 1.0

Use the following details when required:

-   Name of the application: Workplace Space Management
-   ID of the application: sn\_wsd\_spcmgmt

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Space Management\) or ID \(sn\_wsd\_spcmgmt\). If you cannot find the application, you may have to request it from the ServiceNow Store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Space Management.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configuring Workplace Space Management](../concept/configure-space-management.md)

