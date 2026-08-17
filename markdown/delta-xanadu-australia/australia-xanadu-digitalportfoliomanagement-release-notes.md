---
title: Combined Digital Portfolio Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Digital Portfolio Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-digitalportfoliomanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Digital Portfolio Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Digital Portfolio Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Digital Portfolio Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Digital Portfolio Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Digital Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use the Admin Center in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-admin-center&family=xanadu&ft:locale=en-US)**

Use the DPM Admin Center guided walk-through to set up your DPM Workspace. The Admin Center guides you to identify data in your instance that’s ready to view in DPM. Use the provided suggestions to set up and configure the DPM Workspace for that instance. For example, if planning data isn’t used in the instance, then the DPM Admin Center guides you on how to hide the Plan tab. The DPM Admin Center also provides links to appropriate tables to create or edit services, applications, and portfolios. Here are more tasks a DPM administrator can do with the DPM Admin Center.

    -   Use workflows to identify and set up solutions \(services, service offerings, business applications, and application services\). The guided walk-through includes insights into each solution's data readiness for DPM.
    -   Access the settings pages to configure the DPM Workspace using the provided system properties.
    -   Configure solution page headers and the General info section of the Info tab.
    -   Map KPI groups to solutions to view metrics in the DPM Workspace.
    -   Use links to helpful resources.
    -   Refer to common question links to aid implementation.
    -   Follow the prompts for more setup tasks.
-   **[View relationship maps in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-view-relationship-map&family=xanadu&ft:locale=en-US)**

Use the ServiceNow platform Unified Map to see a more holistic and comprehensive view of your service and application relationships. The Unified Map replaces the custom DPM relationship map, but you still access the Unified Map in the context of the DPM Workspace. For more information on the platform map, see [Unified Map](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&family=xanadu&ft:locale=en-US).

-   **[Update KPIs in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-kpi-descriptions&family=xanadu&ft:locale=en-US)**
    -   Update the description of a KPI indicator that's provided by the base system. The KPI indicators on solution records come from Performance Analytics \(PA\). In the DPM Workspace, you can select a tooltip on a solution indicator card to see a description that clarifies the indicator data. Even though the descriptions come with the base system, administrators can update the descriptions to accommodate the organization.
    -   With the June 2024 release and after, the **KPI latest score** system property is set to true for new and zBoot customers.
-   **[Work with Needs attention panels in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-needs-attn-panels&family=xanadu&ft:locale=en-US)**
    -   Added problem \(PRB\) records to the Needs attention attributes so that you can identify problems on the following solutions.
        -   Services and service offerings. Problems are related to the service offering via the service offering record on the form, impacted services related list, and on the affected CIs related list. Problems are then rolled up to the parent service and should be deduplicated at the parent service level.
        -   Business applications. Problems are related to the application service via the configuration item field on the form. Problems are then rolled up from the application service to the business application and should be deduplicated at the parent service level.
        -   Application services. Problems are related to the application service via the configuration item field on the form.
    -   Updated the team logic in the DPM Contacts tab for each solution. When you select the Contacts icon \(\[Omitted image "image.contacts"\] Alt text: Contacts icon.\) next to the Needs attention panel, the Teams tab includes multiple teams that support the record. The multiple team assignment is an existing platform feature that was added to Service Portfolio Management so the teams can be viewed in the DPM Workspace. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Use the Admin Center in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-admin-center&family=yokohama&ft:locale=en-US)**

Use the added Troubleshoot tab on the DPM Admin Center landing page to help you recalculate availability results and indicators for service offerings. You select a specific time period for the recalculation and then you can check the progress in the event log.

-   **[Configure personal portfolio solution cards in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-configure-solution-cards&family=yokohama&ft:locale=en-US)**

Configure the fields that are displayed on the personal portfolio solution cards in the DPM Workspace. Solution cards display information about the four main types of solutions \(service, service offering, business application, and application service\). This configuration determines the fields that are displayed on each solution card.

-   **[View relationships of business applications and application services in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-view-related-records&family=yokohama&ft:locale=en-US)**

See all incidents, problems, and changes that are related to your business applications and application services. You can view the data in these areas:

    -   The DPM Admin Center
    -   In the DPM Workspace, in the Needs attention panels and in the life-cycle tabs that present key performance indicator \(KPI\) data.
-   **[KPI groups in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-configure-kpi&family=yokohama&ft:locale=en-US)**

Added the ability to select the spark lines \(time series chart\) for a KPI indicator to open its details.

-   **[Update KPIs in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-kpi-descriptions&family=yokohama&ft:locale=en-US)**

Added an Active flag so that you can hide KPIs in a KPI group from the DPM Workspace. The Active flag is available for all KPIs so that you can hide an individual KPI even when it's part of a larger KPI group.

-   **[View application service details](https://www.servicenow.com/docs/access?context=dpm-app-service-details&family=yokohama&ft:locale=en-US)**

Expanded the DPM data model so that when an incident, problem, or change is in the application service's Impacted services or Affected CIs related list, the updates roll up to the related business application. You can see the impacts in the related business application's KPIs and Needs attention panels\). For more information, see [Work with Needs attention panels in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-needs-attn-panels&family=yokohama&ft:locale=en-US).

-   **[Work with lists in Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-list-modules&family=yokohama&ft:locale=en-US)**

Use the updated logic in the list address bar to copy the link of any list item to share that list with others. The list address includes a unique list ID for every list item. This updated logic applies wherever lists are used in the DPM Workspace:

    -   In the list module \(for both provided lists and created lists\).
    -   In the DPM Admin Center.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Digital Portfolio Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=xanadu&ft:locale=en-US)**

The Digital Portfolio Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) that follows.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Digital Portfolio Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Digital Portfolio Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Digital Portfolio Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Digital Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Digital Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Digital Portfolio Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=xanadu&ft:locale=en-US) for details.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Digital Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Digital Portfolio Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Introduced the DPM Admin Center to set up the DPM Workspace. The Admin Center includes workflows to identify and set up business and technical services, business applications, and application services. The DPM Admin Center includes guided steps, prompts, and links to solutions and helpful resources.
-   Replaced the custom DPM relationship map with the ServiceNow platform Unified Map to provide a more holistic view of service and application relationships.
-   Updated the key performance indicator \(KPI\) functionality.
    -   Added descriptive KPI tooltips to clarify the indicator data.
    -   Set the system property **KPI latest score** to true for new and zBoot customers.
-   Updated the configuration options for the Needs attention panels.
    -   Added problem \(PRB\) records to the Needs attention attributes.
    -   Updated the team logic in the DPM Contacts tab in the Needs attention panel.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Updated the Digital Portfolio Management \(DPM\) Admin Center.
    -   Added a Troubleshoot tab to the DPM Admin Center landing page to help you recalculate availability results and indicators for service offerings.
    -   Added the ability to configure the personal portfolio solution cards and to view relationships of business applications and application services.
-   Updated the key performance indicator \(KPI\) behavior so that you can drill down on time series KPI information and use an Active flag to hide KPIs in a KPI group.
-   Updated the DPM data model to improve visibility and reporting when an incident, problem, or change is in the application service's Impacted services or Affected CIs related list. The updated model rolls up the incidents, problems, and changes so that you can see the impacts in related business applications \(in the KPIs and Needs attention panels\).

 See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

