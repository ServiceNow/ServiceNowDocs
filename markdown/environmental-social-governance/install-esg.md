---
title: Install Operational Sustainability Management \(formerly ESG Management\)
description: You can install the ESG Management application \(sn\_esg\) if you have the sys\_admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Operational Sustainability Management \(formerly ESG Management\) implementation, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Install Operational Sustainability Management \(formerly ESG Management\)

You can install the ESG Management application \(sn\_esg\) if you have the sys\_admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   ESG Management requires the following ServiceNow Store applications. Ensure that these applications are installed before you install ESG Management.
    -   **Required ServiceNow Store applications**
        -   **GRC: Profiles**

            The GRC: Profiles application is a set of common components shared by the GRC suite of applications. The application includes common architecture, issue management, and indicators.

    -   **GRC: Common Workspace Elements**

        The GRC Base Workspace is the container of all the shared seismic workspace parts among GRC applications.

    -   **Goal Framework**

        The Goal Framework application enables you to add goals that track your progress towards your chosen material topics.

    -   **GRC: Metrics**

        The GRC: Metrics application enables you to define the metrics that are used to assess, compare, track, and report the performance of the other applications.

    -   **Microsoft 365 for ServiceNow Reporting**

        The Microsoft 365 for ServiceNow Reporting \(sn\_esg\_msoff\_intg\) provides disclosure reporting capabilities to ESG reporting managers to seamlessly report ServiceNow ESG Management system data, list reports, charts, pivot, and multi pivot reports using Microsoft Word.


**Note:** With the ESG Management application, you can use the authority documents and citations in the GRC: Policy and Compliance Management application and entities in the GRC: Profiles application.

Role required: admin

## About this task

The following items are installed with ESG Management:

-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../reference/components-installed-with-esg.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ESG Management application \(sn\_esg\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install ESG Management.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Operational Sustainability Management \(formerly ESG Management\) implementation](../concept/esg-implementation.md)

