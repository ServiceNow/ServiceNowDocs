---
title: Install ServiceNow Voice for CSM
description: You can install the ServiceNow Voice for CSM application \(sn\_cti\_csm\_cnt\) if you have the admin role. The application installs related ServiceNow Store applications if they are not already installed.
locale: en-US
release: zurich
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Integrating ServiceNow Voice with CSM, Integrating with applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install ServiceNow Voice for CSM

You can install the ServiceNow Voice for CSM application \(sn\_cti\_csm\_cnt\) if you have the admin role. The application installs related ServiceNow® Store applications if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   ServiceNow Voice for CSM requires the following ServiceNow Store applications. Ensure that this application is installed before you install ServiceNow Voice for CSM.
    -   **Required ServiceNow Store applications**
        -   **Customer Service plugin \(com.sn\_customerservice\)**

            Installs the Customer Service Management application.

        -   **Amazon Connect Integration with ServiceNow Voice \(sn\_cti\_amzn\_cct\)**

            Integrates the ServiceNow instance with the Amazon Connect server.


Role required: admin

## About this task

The following items are installed with ServiceNow Voice for CSM:

-   Contact flows
-   Operation handlers

For more information, see [Components installed with ServiceNow Voice for CSM](../reference/instld-with-ccc-csm.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ServiceNow Voice for CSM application \(sn\_cti\_csm\_cnt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install ServiceNow Voice for CSM.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

To set up Voice for CSM, see [Setting up ServiceNow Voice](../concept/ccc-setup.md)

**Parent Topic:**[Integrating ServiceNow Voice with CSM](../concept/integrating-ccc-csm.md)

