---
title: Install Workplace Connectors
description: Install the Workplace Connectors application from the ServiceNow Store.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Connectors

Install the Workplace Connectors application from the ServiceNow Store.

## Before you begin

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Ensure you have the following plugins:

-   Workplace Connectors
-   Workplace Central
-   Workplace Core

Complete the following setup instructions:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance.

    The list displays the subscriptions that your organization has purchased.


Use the following details when required:

-   Name of the application: Workplace Connectors
-   Application ID: sn\_wsd\_wc

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Connectors or ID \(sn\_wsd\_wc\). If you can’t find the application, you may have to request it from the ServiceNow Store.

3.  Select **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed. If there are any plugins or applications that must be installed, you must install them before you can install Workplace Space Management.

5.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Select **Install**.


**Parent Topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Previous topic:**[Configure Workplace Connectors](configure-workplace-connectors.md)

**Next topic:**[Configure sensor data providers](../task/providers-occupancy.md)

