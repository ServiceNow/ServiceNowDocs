---
title: Install Idea Manager dashboard
description: You can install the Idea Manager dashboard application from ServiceNow Store if you have the admin role. This application includes demo data and installs the related plugins if they are not already installed.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Innovation Management, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Install Idea Manager dashboard

You can install the Idea Manager dashboard application from ServiceNow Store if you have the admin role. This application includes demo data and installs the related plugins if they are not already installed.

## Before you begin

**Note:** Starting with version 2.0.0, the Idea Manager dashboard is available in the Next experience UI Framework which can be accessed from Analytics Idea Manager.

-   Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If the application requires plugins or other store applications, install them first if they are not already installed. For the Idea Manager dashboard application, the following plugins are required:
    -   PPM Standard plugin \(com.snc.financial\_planning\_pmo\)

        For information on activation steps, see [Activate PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/task/t_ActivateProjectPortfolioSuiteWithFinancials.md).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## Result

You can access the Idea Manager dashboard by navigating to **Ideas** &gt; **Idea Manager Dashboard**.

## What to do next

Run the following Performance Analytics data collector jobs before using the Idea Manager dashboard.

-   **\[PA PPM IMD\] Historic Data Collection**: Collects historical data related to ideas and runs on demand to update data for dashboard.
-   **\[PA PPM IMD\] Daily Data Collection**: Collects data for daily indicators and runs daily to update data for dashboard.

**Parent Topic:**[Configuring Innovation Management](../concept/configuring-innovation-management.md)

**Related topics**  


[List of plugins \(Australia\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

