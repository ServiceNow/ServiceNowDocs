---
title: Digital Portfolio Management \(DPM\) release notes
description: The ServiceNow Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Digital Portfolio Management \(DPM\) release notes

The ServiceNow® Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.

## Digital Portfolio Management \(DPM\) highlights for the Zurich release

-   Configurable Info tab allows customers to configure the Info tab of the solutions pages, similarly to how they can configure the Plan, Build, and Run tabs.
    -   This includes showing or hiding sections of the tab.
-   DPM users with the dpm\_admin role can now create and edit portfolios directly within DPM, and three portfolio templates are included \("EDUCAUSE", "IT Service Portfolio", and "Sample Organization Structure"\).
-   DPM users can now send an email to any users with the dpm\_manager role that includes the first key performance indicator \(KPI\) group data and a link back to the solution they're sending an email from.
    -   This feature is off by default and can be activated in the DPM Admin Center under a new 'Email properties' section.
-   DPM admins can turn on a scheduled job that will automatically send the top KPI group data in an email to the solution owners.
    -   The schedule is configurable and will only send KPI data for the 'top level objects' that a user owns. For example, if they own a taxonomy node, it won't send data on sub nodes or services.
    -   DPM users can now view more than one KPI group in the Enterprise Portfolio preview.
-   DPM users with the dpm\_admin role can use the Active flag to hide or show the portfolio and taxonomy node branches in the Enterprise Portfolio Module.
    -   DPM admins can set an enterprise portfolio's **Status** to Active or Inactive.
    -   DPM managers will only see enterprise portfolios that are active.

See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

**Important:** Digital Portfolio Management \(DPM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Configure the Info tab in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-configure-info-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Show or hide various sections of the **Info** tab for your solutions in DPM.

-   **[Create enterprise service portfolios using a template](https://www.servicenow.com/docs/access?context=dpm-create-enterprise-portfolio-using-template&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Create enterprise portfolios from scratch or by using a template. Enterprise portfolios are structured in a nesting tree format to facilitate navigation of service-related items and taxonomy nodes. Similar to personal portfolios, you can see key metrics to assess the portfolio performance.

-   **[Configure scheduled email reports in DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-schedule-email-reports&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Send periodic emails of KPI metrics to the DPM solution owners. This feature is off by default and can be activated in the DPM Admin Center under a new 'Email properties' section.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **Enhancements to the Web and installed apps monitoring setup**

    The process of adding an application for monitoring has been updated to enable you to choose any service from the cmdb\_ci\_service table or its child tables. The application type filed was added to the monitored applications list.


## Activation information

Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Use the ServiceNow® Service Portfolio Management application to set up and manage your services and offerings, and then organize them in portfolios. In the Digital Portfolio Management application, you can view the health and status of those portfolios and track them in one centralized location.

-   **[Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Use ServiceNow® Performance Analytics to create reports on key performance indicators \(KPIs\) to monitor and analyze metrics.

-   **[Digital Portfolio Management related applications and data sources](https://www.servicenow.com/docs/access?context=dpm-related-products&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Other related ServiceNow applications bring in data from your services, service offerings, business applications, and application services for you to view all of them in your unified workspace view. All the related applications are optional and aren't required to use Digital Portfolio Management. This topic also offers links to Knowledge Base articles with more data source information.

-   **[Service Builder](https://www.servicenow.com/docs/access?context=service-builder&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As you view service information in Digital Portfolio Management, you can create and edit services and service offerings with quick access to the ServiceNow® Service Builder application.

    **Important:** If you use Service Builder and plan to upgrade to the current version of DPM, you must also upgrade to the current version of Service Builder at the same time.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

