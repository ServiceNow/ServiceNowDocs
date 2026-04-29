---
title: Install Workplace Maintenance Management
description: Install the Workplace Maintenance Management \( application from the ServiceNow Store. Visit the ServiceNow Store to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: australia
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Maintenance Management, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Maintenance Management

Install the Workplace Maintenance Management \( application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Installing Workplace Maintenance Management \(sn\_wsd\_maintenance\) activates/installs the following:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance.

    The list displays the subscriptions that your organization has purchased.

2.  Verify that the following plugins are activated:
    -   Workplace Core \(sn\_wsd\_core\)
    -   Workplace Central \(sn\_wsd\_central\)
    -   Enterprise Model and Asset Classes \(sn\_ent\)
    -   Workplace Case Management \(sn\_wsd\_case\)
    -   Workplace Move Management

Use the following details when required:

-   Name of the application: Workplace Maintenance Management
-   ID of the application: sn\_wsd\_maintenance

Role required: sn\_wsd\_maintenance.admin

## About this task

**Note:** Activate Workplace Central plugin \(sn\_wsd\_central\) and ensure you have the role sn\_wsd\_maintenance.admin assigned.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Maintenance Management or ID \[sn\_wsd\_maintenance\]\). If you cannot find the application, you may have to request it from the ServiceNow Store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you install Workplace Maintenance Management.


## Result

Workplace Maintenance Management is installed.

**Parent Topic:**[Configuring Maintenance Management](../concept/configure-maintenance-mgmt.md)

**Previous topic:**[Configuring Maintenance Management](../concept/configure-maintenance-mgmt.md)

**Next topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

