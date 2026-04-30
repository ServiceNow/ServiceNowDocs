---
title: Install EMR Help
description: You can install the EMR Help application \(sn\_ind\_rmt\_help\) if you have the admin role. The application includes demo data.
locale: en-US
release: zurich
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Install EMR Help

You can install the EMR Help application \(sn\_ind\_rmt\_help\) if you have the admin role. The application includes demo data.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Confirm that a ServiceNow ITSM Healthcare and Life Sciences Service Management Core package is already installed by an administrator.

Role required: admin

## About this task

The following items are installed with EMR Help:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with EMR Help](../reference/components-installed-emr-help.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the EMR Help application \(sn\_ind\_rmt\_help\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    If dependent plugins and applications are listed then they will be installed, are currently installed, or need to be installed. If any plugins or applications must be installed, you must install them before you can install the EMR Help application.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


