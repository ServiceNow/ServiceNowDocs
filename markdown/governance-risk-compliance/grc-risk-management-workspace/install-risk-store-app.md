---
title: Install Risk Management
description: You can install the Risk Management application \(com.sn\_risk\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Risk Management implementation, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Install Risk Management

You can install the Risk Management application \(com.sn\_risk\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Risk Management requires the following plugins. Ensure that these plugins are activated before you install Risk Management.
    -   **Required ServiceNow plugins**
        -   **GRC Risk Management dependencies**

            Installs all the dependent plugins required to support the GRC Risk Management application.

-   Risk Management requires the following ServiceNow Store applications. Ensure that these applications are installed before you install Risk Management.
    -   **Required ServiceNow Store applications**
        -   **GRC Profiles**

            The GRC: Profiles application is a set of common components shared by the GRC suite of applications. The application includes common architecture, issue management, and indicators.


Role required: admin

## About this task

The following items are installed with Risk Management:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Risk Management](../reference/r_InstallWRisk.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Risk Management application \(com.sn\_risk\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install .

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Risk Management implementation](../concept/risk-impl-overview.md)

