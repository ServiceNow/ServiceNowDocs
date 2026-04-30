---
title: Install Financial Services Client Lifecycle
description: You can install the Financial Services Client Lifecycle application \(sn\_bom\_clo\_b2c\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Install Financial Services Client Lifecycle

You can install the Financial Services Client Lifecycle application \(sn\_bom\_clo\_b2c\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with Financial Services Client Lifecycle:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with Financial Services Client Lifecycle](../reference/installed-with-client-lifecycle.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Financial Services Client Lifecycle application \(sn\_bom\_clo\_b2c\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Financial Services Client Lifecycle.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Install Financial Services Customer Lifecycle Operations](../concept/set-up-customer-lifecycle-ops.md)

