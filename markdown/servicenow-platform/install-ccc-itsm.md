---
title: Install ServiceNow Voice for ITSM
description: You can install the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\) if you have the admin role. This plugin installs the ITSM content for integration between ServiceNow Voice and a third-party phone system.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow Voice with ITSM, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install ServiceNow Voice for ITSM

You can install the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\) if you have the admin role. This plugin installs the ITSM content for integration between ServiceNow Voice and a third-party phone system.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Your organization must have purchased ITSM Pro subscription, which includes the ServiceNow Voice SKU.
-   ServiceNow Voice for ITSM requires the following ServiceNow Store application. Ensure that this application is installed before you install ServiceNow Voice for ITSM.
    -   **Required ServiceNow Store applications**
        -   **Amazon Connect Integration with ServiceNow Voice \(sn\_cti\_amzn\_cct\)**

            Integrates the ServiceNow instance with the Amazon Connect server.


Role required: admin

## About this task

The following items are installed with ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\):

-   Contact flows
-   Operation handlers

For more information, see [Components installed with ServiceNow Voice for ITSM](../reference/instld-with-cloud-call-center-itsm.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install ServiceNow Voice for ITSM application \(sn\_cti\_itsm\_cnt\).

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Integrating ServiceNow Voice with ITSM](../concept/integrate-ccc-itsm.md)

