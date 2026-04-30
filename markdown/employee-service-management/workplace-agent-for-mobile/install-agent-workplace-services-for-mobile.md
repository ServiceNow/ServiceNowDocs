---
title: Install Workplace Agent for mobile
description: Install the Workplace Agent for mobile application from ServiceNow Store applications. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: zurich
product: Workplace Agent for mobile
classification: workplace-agent-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Agent for mobile, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Agent for mobile

Install the Workplace Agent for mobile application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup instructions:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance.

    The list displays the subscriptions that your organization has purchased.

2.  Verify that the following plugins are activated:
    -   Workplace Core \(sn\_wsd\_core\)
    -   Workplace Case Management \(sn\_wsd\_case\)
    -   Workplace Maintenance Management \(sn\_wsd\_maintenance\)
    -   Workplace Move Management \(sn\_wsd\_move\)
    -   Workplace Indoor Mapping \(sn\_wsd\_indoor\_map\)
    -   Expanded Model and Asset Classes\(sn\_ent\)

Use the following details when required:

-   Name of the application: Workplace Agent for mobile
-   ID of the application: sn\_wsd\_agent\_mob

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Case Management.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Agent for mobile](../concept/configure-workplace-mobile-agent.md)

