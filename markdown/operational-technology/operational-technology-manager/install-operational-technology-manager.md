---
title: Install Operational Technology Manager
description: If you have the admin role, you can install the Operational Technology Manager application. The application includes demo data and installs that are related ServiceNow Store applications and plugins, if they are not already installed.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Manager, Operational Technology]
---

# Install Operational Technology Manager

If you have the admin role, you can install the Operational Technology Manager application. The application includes demo data and installs that are related ServiceNow® Store applications and plugins, if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

**Note:** To learn more about the subscriptions required for the Operational Technology Manager, see [Subscriptions for Operational Technology Management \(OTM\)](../../operational-technology-management/concept/otm-license-module.md)

Role required: admin

## About this task

The following items are installed with Operational Technology Manager:

-   Plugins
-   Store applications
-   Roles
-   Tables
-   Script includes

For more information on viewing components that are installed with Operational Technology Manager, see [Components installed with Operational Technology Manager](../reference/components-installed-with-operational-technology-manager.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Operational Technology Manager application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they will be installed, are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install Operational Technology Manager.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Configuring the Operational Technology Manager](../concept/configuring-operational-technology-manager.md)

