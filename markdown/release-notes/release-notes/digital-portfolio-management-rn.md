---
title: Digital Portfolio Management \(DPM\) release notes
description: The ServiceNow Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.The ServiceNow Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Digital Portfolio Management \(DPM\) release notes

The ServiceNow® Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.

## About Digital Portfolio Management \(DPM\)

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

See [Digital Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dpm-landing.md) for more information.

## Activation and other requirements

**Important:** Digital Portfolio Management \(DPM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-service-management-rn-landing.md)

## Zurich

The ServiceNow® Digital Portfolio Management \(DPM\) enables you to view and manage the full life cycle of your services and applications. DPM was enhanced and updated in the Zurich release.

### What's new

-   **[Configure the Info tab in the DPM Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dpm-configure-info-tab.md)**

    Show or hide various sections of the **Info** tab for your solutions in DPM.

-   **[Create enterprise service portfolios using a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dpm-create-enterprise-portfolio-using-template.md)**

    Create enterprise portfolios from scratch or by using a template. Enterprise portfolios are structured in a nesting tree format to facilitate navigation of service-related items and taxonomy nodes. Similar to personal portfolios, you can see key metrics to assess the portfolio performance.

-   **[Configure scheduled email reports in DPM Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dpm-schedule-email-reports.md)**

    Send periodic emails of KPI metrics to the DPM solution owners. This feature is off by default and can be activated in the DPM Admin Center under a new 'Email properties' section.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **Enhancements to the Web and installed apps monitoring setup**

    The process of adding an application for monitoring has been updated to enable you to choose any service from the cmdb\_ci\_service table or its child tables. The application type filed was added to the monitored applications list.


