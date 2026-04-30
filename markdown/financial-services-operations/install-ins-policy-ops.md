---
title: Install Personal Lines Servicing
description: You can install the Personal Lines Servicing \(sn\_ins\_policy\_b2c\) application if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Personal Lines Servicing, Personal Lines Servicing, Property and Casualty Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Install Personal Lines Servicing

You can install the Personal Lines Servicing \(sn\_ins\_policy\_b2c\) application if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Personal Lines Servicing](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8117d88f53a220108f12ddeeff7b121e) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Personal Lines Servicing.

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with Personal Lines Servicing](../reference/installed-with-ins-policy-ops.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find your Personal Lines Servicing application \(sn\_ins\_policy\_b2c\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Personal Lines Servicing.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Personal Lines Servicing](../concept/fso-ins-personal-policy-ops-landing-page.md)

