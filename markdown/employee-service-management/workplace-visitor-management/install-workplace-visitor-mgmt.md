---
title: Install Workplace Visitor Management
description: Install the Workplace Visitor Management application from ServiceNow Store applications. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: xanadu
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Workplace Visitor Management, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Visitor Management

Install the Workplace Visitor Management application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup instructions.

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.
2.  Verify that the following plugins are activated:
    -   Workplace Core \(sn\_wsd\_core\) minimum version 2.0.3.
    -   Workplace Visitor Management \(sn\_wsd\_visitor\)

Role required: admin

Use the following details when required:

-   Name of the application: Workplace Visitor Management
-   ID of the application: sn\_wsd\_visitor

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    Search for the application by its name \(Workplace Visitor Management\) or ID \(sn\_wsd\_visitor\). If you cannot find the application, you may have to request it from ServiceNow store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Visitor Management.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Visitor Management](../concept/configure-visitor-mgmt.md)

**Related topics**  


[Create a visitor policy](create-visitor-policy.md)

[Create a record producer for visitor management](create-rec-prodcr-visit-mgmt.md)

[Create a visitor badge template](create-visitor-badge-template.md)

[Configuring Workplace Visitor Management for Workplace Services Kiosk](../concept/config-visitor-for-kiosk.md)

[Quick start test for Workplace Visitor Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-wsd-visitor-mgmt.md)

