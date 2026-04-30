---
title: Install the GRC integration with Thomson Reuters Regulatory Intelligence application
description: Install the GRC integration with Thomson Reuters Regulatory Intelligence application \(com.sn\_grc\_int\_tr\). The application includes demo data. It installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with Thomson Reuters Regulatory Intelligence \(TRRI\), GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# Install the GRC integration with Thomson Reuters Regulatory Intelligence application

Install the GRC integration with Thomson Reuters Regulatory Intelligence application \(com.sn\_grc\_int\_tr\). The application includes demo data. It installs related ServiceNow Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

The GRC integration with Thomson Reuters Regulatory Intelligence requires the ServiceNow® Regulatory Change Management application from the ServiceNow Store. Ensure that this application is installed before you install the GRC integration with Thomson Reuters Regulatory Intelligence application.

Role required: sn\_grc\_reg\_change.admin

## About this task

The following items are installed with the GRC integration with Thomson Reuters Regulatory Intelligence application:

-   Store applications
-   Scheduled jobs
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the GRC integration with Thomson Reuters Regulatory Intelligence application \(com.sn\_grc\_int\_tr\) by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, then you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, then you must install them before you can install the GRC integration with Thomson Reuters Regulatory Intelligence application.

4.  Select **Install**.


**Parent Topic:**[GRC integration with Thomson Reuters Regulatory Intelligence](../concept/grc-trri-integration.md)

