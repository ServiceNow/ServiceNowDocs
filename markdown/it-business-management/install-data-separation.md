---
title: Install Data Separation
description: You can install the Data Separation application \(sn\_ds\) if you have the admin role.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Data Separation, Strategic Portfolio Management]
---

# Install Data Separation

You can install the Data Separation application \(sn\_ds\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Data Separation requires the following plugin and store application. Ensure that the following plugin and application is activated before you install Data Separation.
    -   **Required ServiceNow plugin**
        -   **PPM Standard plugin \(com.snc.financial\_planning\_pmo\)**

            Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) in your ServiceNow instance before you install Data Separation. For more information see, [Activate PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/task/t_ActivateProjectPortfolioSuiteWithFinancials.md).

    -   **Required ServiceNow Store application**
        -   **Portfolio Planning \(sn\_align\_ws\)**

            Install the Portfolio Planning \(sn\_align\_ws\) application in your ServiceNow instance before you install Data Separation. For more information see, [Install Portfolio Planning](../../portfolio-planning/task/install-portfolio-planning.md).


Role required: admin

## About this task

The following items are installed with Data Separation:

-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with Data Separation](../reference/installed-with-data-separation.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Data Separation application \(sn\_ds\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they’ll be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Data Separation.

4.  Select **Install**.


**Parent Topic:**[Configuring Data Separation](../concept/configuring-data-separation.md)

