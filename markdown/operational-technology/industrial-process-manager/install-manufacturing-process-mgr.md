---
title: Install the Industrial Process Manager
description: If you have the required entitlement and the Administrator \[admin\] role, you can install the Industrial Process Manager application and the related plugins.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Process Manager, Operational Technology]
---

# Install the Industrial Process Manager

If you have the required entitlement and the Administrator \[admin\] role, you can install the Industrial Process Manager application and the related plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with the Industrial Process Manager:

-   Plugins
-   Application menu, including Guided Setup
-   Roles
-   Tables

For more information on viewing the components that are installed with the Industrial Process Manager application, see [Components installed with Industrial Process Manager](../reference/components-installed-with-industrial-process-manager.md).

**Note:** For Operational Technology Service Management users with no license for Operational Technology Visibility, note the following:

-   When you have the latest version of Operational Technology Incident Management installed, Industrial Process Manager is also installed.
-   When you have the latest version of Operational Technology Change Management installed, Industrial Process Manager is also installed.

You should upgrade to the latest versions so you have access to the Operational Technology Service Management experience.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Industrial Process Manager application by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they will be installed, are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install the Industrial Process Manager.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Configuring the Industrial Process Manager](../concept/configuring-manufacturing-process-mgr.md)

