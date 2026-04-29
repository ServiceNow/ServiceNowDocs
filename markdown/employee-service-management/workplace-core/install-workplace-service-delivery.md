---
title: Install Workplace Core
description: You can install the Workplace Core application if you have the admin role. This application includes optional demo data.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Workplace Core, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Core

You can install the Workplace Core application if you have the admin role. This application includes optional demo data.

## Before you begin

Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following components are installed with installation of the Workplace Core application:

-   Roles
-   Tables

See [Components installed with Workplace Core](../reference/components-installed-with-workplace-service-delivery.md) for more information.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they are not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they are not installed already.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Some applications include demo data, which are sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Note:** If you don't load the demo data for a store application during installation, it is not available to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Core](../concept/configure-wsd.md)

**Related topics**  


[Providing your workplace data](../concept/providing-your-workplace-data-wsd.md)

[Configuring spreadsheets to import workplace data](../concept/importing-workspace-data-wsd.md#)

[Activate Virtual Agent for Workplace Service Delivery](actuvate-va-for-wsd.md)

