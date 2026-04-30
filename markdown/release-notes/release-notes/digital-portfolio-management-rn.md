---
title: Digital Portfolio Management release notes
description: The ServiceNow Digital Portfolio Management Workspace enables you to view and manage the full life cycle of your services and applications. The Digital Portfolio Management Workspace was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
---

# Digital Portfolio Management release notes

The ServiceNow® Digital Portfolio Management Workspace enables you to view and manage the full life cycle of your services and applications. The Digital Portfolio Management Workspace was enhanced and updated in the Xanadu release.

## Digital Portfolio Management highlights for the Xanadu release

-   Introduced the DPM Admin Center to set up the DPM Workspace. The Admin Center includes workflows to identify and set up business and technical services, business applications, and application services. The DPM Admin Center includes guided steps, prompts, and links to solutions and helpful resources.
-   Replaced the custom DPM relationship map with the ServiceNow platform Unified Map to provide a more holistic view of service and application relationships.
-   Updated the key performance indicator \(KPI\) functionality.
    -   Added descriptive KPI tooltips to clarify the indicator data.
    -   Set the system property **KPI latest score** to true for new and zBoot customers.
-   Updated the configuration options for the Needs attention panels.
    -   Added problem \(PRB\) records to the Needs attention attributes.
    -   Updated the team logic in the DPM Contacts tab in the Needs attention panel.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

**Important:** Digital Portfolio Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Use the Admin Center in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-admin-center&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the DPM Admin Center guided walk-through to set up your DPM Workspace. The Admin Center guides you to identify data in your instance that’s ready to view in DPM. Use the provided suggestions to set up and configure the DPM Workspace for that instance. For example, if planning data isn’t used in the instance, then the DPM Admin Center guides you on how to hide the Plan tab. The DPM Admin Center also provides links to appropriate tables to create or edit services, applications, and portfolios. Here are more tasks a DPM administrator can do with the DPM Admin Center.

    -   Use workflows to identify and set up solutions \(services, service offerings, business applications, and application services\). The guided walk-through includes insights into each solution's data readiness for DPM.
    -   Access the settings pages to configure the DPM Workspace using the provided system properties.
    -   Configure solution page headers and the General info section of the Info tab.
    -   Map KPI groups to solutions to view metrics in the DPM Workspace.
    -   Use links to helpful resources.
    -   Refer to common question links to aid implementation.
    -   Follow the prompts for more setup tasks.
-   **[View relationship maps in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-view-relationship-map&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the ServiceNow platform Unified Map to see a more holistic and comprehensive view of your service and application relationships. The Unified Map replaces the custom DPM relationship map, but you still access the Unified Map in the context of the DPM Workspace. For more information on the platform map, see [Unified Map](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **[Update KPIs in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-kpi-descriptions&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Update the description of a KPI indicator that's provided by the base system. The KPI indicators on solution records come from Performance Analytics \(PA\). In the DPM Workspace, you can select a tooltip on a solution indicator card to see a description that clarifies the indicator data. Even though the descriptions come with the base system, administrators can update the descriptions to accommodate the organization.
    -   With the June 2024 release and after, the **KPI latest score** system property is set to true for new and zBoot customers.
-   **[Work with Needs attention panels in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-needs-attn-panels&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Added problem \(PRB\) records to the Needs attention attributes so that you can identify problems on the following solutions.
        -   Services and service offerings. Problems are related to the service offering via the service offering record on the form, impacted services related list, and on the affected CIs related list. Problems are then rolled up to the parent service and should be deduplicated at the parent service level.
        -   Business applications. Problems are related to the application service via the configuration item field on the form. Problems are then rolled up from the application service to the business application and should be deduplicated at the parent service level.
        -   Application services. Problems are related to the application service via the configuration item field on the form.
    -   Updated the team logic in the DPM Contacts tab for each solution. When you select the Contacts icon \(![Contacts icon.](../../product/digital-portfolio-management/image/contacts.png)\) next to the Needs attention panel, the Teams tab includes multiple teams that support the record. The multiple team assignment is an existing platform feature that was added to Service Portfolio Management so the teams can be viewed in the DPM Workspace. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Changed in this release

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    The Digital Portfolio Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [Accessibility information](digital-portfolio-management-rn.md#digital-portfolio-management-rn-accessibility) that follows.


## Activation information

Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


## Related ServiceNow applications and features

-   **[Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the ServiceNow® Service Portfolio Management application to set up and manage your services and offerings, and then organize them in portfolios. In the Digital Portfolio Management application, you can view the health and status of those portfolios and track them in one centralized location.

-   **[Service Builder](https://www.servicenow.com/docs/access?context=service-builder&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    As you view service information in Digital Portfolio Management, you can create and edit services and service offerings with quick access to the ServiceNow® Service Builder application.

    **Important:** If you use Service Builder and plan to upgrade to the current version of DPM, you must also upgrade to the current version of Service Builder at the same time.

-   **[Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Use ServiceNow® Performance Analytics to create reports on key performance indicators \(KPIs\) to monitor and analyze metrics.

-   **[Digital Portfolio Management related applications and data sources](https://www.servicenow.com/docs/access?context=dpm-related-products&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Other related ServiceNow applications bring in data from your services, service offerings, business applications, and application services for you to view all of them in your unified workspace view. All the related applications are optional and aren't required to use Digital Portfolio Management. This topic also offers links to Knowledge Base articles with more data source information.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

