---
title: Install Workplace Concierge
description: Install the Workplace Concierge application from the ServiceNow Store. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: zurich
product: Workplace Concierge
classification: workplace-concierge
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Concierge

Install the Workplace Concierge application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup instructions:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance.

    The list displays the subscriptions that your organization has purchased.

2.  Verify that the Workplace Core plugin is activated.

Use the following details when required:

-   Name of the application: Workplace Concierge
-   ID of the application: sn\_wsd\_concierge

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Concierge or ID \(sn\_wsd\_concierge\). If you cannot find the application, you may have to request it from the ServiceNow Store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Concierge.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Concierge](../concept/configure-workplace-concierge.md)

**Related topics**  


[Configure calendar sections on the Presence dashboard](configure-presence-dashboard-sections.md)

[Configure workplace space suggestions for employees](../concept/configure-workplace-suggestions.md)

