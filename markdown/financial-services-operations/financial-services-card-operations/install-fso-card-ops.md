---
title: Install Financial Services Card Operations
description: You can install the Financial Services Card Operations application \(sn\_bom\_credit\_card\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Install Financial Services Card Operations

You can install the Financial Services Card Operations application \(sn\_bom\_credit\_card\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with Financial Services Card Operations:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Financial Services Card Operations](../reference/installed-with-card-operations.md).

**Note:** To enable customers to submit requests through the Consumer Service Portal, you should also activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Financial Services Card Operations application \(sn\_bom\_credit\_card\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Financial Services Card Operations.

4.  Select **Install**.


