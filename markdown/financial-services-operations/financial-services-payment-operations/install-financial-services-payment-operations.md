---
title: Install Financial Services Payment Operations
description: Install the Financial Services Payment Operations \(sn\_bom\_payment\) application if you have the admin role. This application includes demo data and installs the related store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Install Financial Services Payment Operations

Install the Financial Services Payment Operations \(sn\_bom\_payment\) application if you have the admin role. This application includes demo data and installs the related store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If the application requires plugins or other store applications, install them first if they are not already installed.

Role required: admin

## About this task

The following items are installed with the installation of the Financial Services Payment Operations application:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Financial Services Payment Operations](../reference/installed-with-payment-operations.md).

**Note:** To enable customers to submit requests through the Consumer Service Portal, you should also activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Financial Services Payment Operations application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Related topics**  


[bundle-platadm.list-of-plugins]

