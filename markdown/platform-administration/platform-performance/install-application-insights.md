---
title: Install Application Insights
description: You can install the Application Insights application \(sn\_app\_insights\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Install Application Insights

You can install the Application Insights application \(sn\_app\_insights\) if you have the admin role.

## Before you begin

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Application Insights requires the following plugin.

    -   **Required ServiceNow plugins**
        -   **MetricBase \(com.snc.clotho\)**

            You must request the MetricBase \(com.snc.clotho\) plugin from Now Support before you install Application Insights.

    **Important:** The MetricBase plugin must be activated by ServiceNow personnel via a Catalog Item request, in order to properly install and configure the ClothoDB. If you attempt to activate MetricBase on the instance yourself, the ClothoDB is not provisioned and Application Insights displays a 500: Internal Server Error.

    If you need this plugin activated in more than one instance, you must submit separate requests for each instance.


Role required: admin

## About this task

The following items are installed with Application Insights:

-   Roles
-   Tables

For more information, see [Components installed with Application Insights](../reference/installed-with-app-insights.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Application Insights application \(sn\_app\_insights\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed.

4.  Select **Install**.


-   **[Components installed with Application Insights](../reference/installed-with-app-insights.md)**  
Several types of components are installed with the installation of the Application Insights application, including tables and user roles.

**Parent Topic:**[Application Insights](../concept/application-insights.md)

