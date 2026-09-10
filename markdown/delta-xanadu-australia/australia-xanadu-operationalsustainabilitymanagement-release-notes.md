---
title: Combined Operational Sustainability Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Operational Sustainability Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-operationalsustainabilitymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Operational Sustainability Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Operational Sustainability Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Sustainability Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Sustainability Management to Australia

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

Between your current release family and Australia, new features were introduced for Operational Sustainability Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Track scope 3 emissions](https://www.servicenow.com/docs/access?context=scope-3-dashboard&family=xanadu&ft:locale=en-US)**

Track Scope 3 emissions using the Scope 3 dashboard to fully grasp and manage your organization's environmental impact. These emissions constitute the largest part of your greenhouse gas output, stemming from indirect sources. This comprehensive understanding aids in regulatory compliance, and obtaining full carbon footprint disclosures. After you identify your scope 3 emission sources, you can take action to mitigate the largest sources of indirect emissions.

-   **[View emission factors in ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&family=xanadu&ft:locale=en-US)**

Use the Unified content management to automatically obtain the emission factors that are published by the standard sources. Emission factors are coefficients that quantify the emissions produced per unit of activity, material, or energy consumption. They’re crucial for calculating the amount of greenhouse gases \(GHGs\) or pollutants emitted into the atmosphere based on various activities.

-   **[Create fiscal calendars to collect metrics from different geographical locations](https://www.servicenow.com/docs/access?context=enable-custom-fiscal-year&family=xanadu&ft:locale=en-US)**

Collect, aggregate, and report data according to your fiscal calendars that could be different from the standard Gregorian calendar. Many global organizations might have operations in different countries that could follow their own fiscal calendars. This feature enables the entities in other locations to collect data according to their own fiscal calendars.

-   **[Choose the approval flow for metrics](https://www.servicenow.com/docs/access?context=components-installed-with-esg&family=xanadu&ft:locale=en-US)**

Set the sn\_esg.metric\_approval property to use either a simple approval flow for your metrics and metric definitions or use the GRC: Approver Configurator to define multiple levels of approvals based on the business rule definitions. This property has two choices.

If you choose the **Simple** option, the Approval section is enabled both on the manual metric definition form and within the metrics. Using this section, you can designate approvers directly on the metric definition form. This option has a single level of approval.

If you choose the **Advanced** option, the Approval section is unavailable on the manual metric definition form and within the metrics, helping to prevent you from assigning approvers there. Instead, approval can be obtained by setting the approval conditions, tables, and approvers in the GRC: Approver Configurator application. This application also enables you to define multiple levels of approvals.

-   **[Create ad hoc metric data tasks](https://www.servicenow.com/docs/access?context=create-an-adhoc-metric-data-task&family=xanadu&ft:locale=en-US)**

Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.

-   **[Metric data table](https://www.servicenow.com/docs/access?context=metric-data-table&family=xanadu&ft:locale=en-US)**

Use the enhanced filters on the metric data table to filter your tasks. The filters help to show only the relevant and open tasks for data owners and approvers.

-   **[Identify the energy usage and emission of every asset](https://www.servicenow.com/docs/access?context=managing-sustainable-it&family=xanadu&ft:locale=en-US)**

Use the Sustainable IT dashboard to explore models within a specific category and view the energy consumption of each asset model and all its assets, listed in descending order. This functionality provides deeper insights into your energy usage, helping you identify the models that are in use and are consuming the most energy.


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
</table>## Changes

Between your current release family and Australia, some changes were made to existing Operational Sustainability Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[ESG program manager role enhanced](https://www.servicenow.com/docs/access?context=components-installed-with-esg&family=xanadu&ft:locale=en-US)**

The ESG program manager \(sn\_esg.program\_manager\) can now create, read, update, and delete emission factors.

-   **Changes in the metric tables**

Enhanced the following metric related tables with read access control lists \(ACLs\):

    -   Metric definition
    -   Metric
    -   Metric data
    -   Metric data task
    -   Metric data task url
With this change, the following changes are in effect:

    -   Metric level Approver user or Approver group: This means that the specified user or group designated as the approver can access only the particular metric and the tables specified for which they are the approver.
    -   Multi-level approval: This means that the specified user or group designated as the approver can access only those records in the metric related tables for which they are the approver.
    -   Enable enterprise owners to access metric records: This means that an enterprise owner can access any metric related record.

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

Between your current release family and Australia, some Operational Sustainability Management features or functionality were removed.

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

Between your current release family and Australia, some Operational Sustainability Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Starting with the Xanadu release, the Global Reporting Initiative \(GRI\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The Unified content management application provides the latest experience for this functionality.
-   Starting with the Xanadu release, the Sustainability Accounting Standards Board \(SASB\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The Unified content management application provides the latest experience for this functionality.

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

Review information on how to activate Operational Sustainability Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Operational Sustainability Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Sustainability Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Operational Sustainability Management we have noted them here.

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

Review details on accessibility information for Operational Sustainability Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Operational Sustainability Management we have noted them here.

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

If there are specific highlight considerations for Operational Sustainability Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Track Scope 3 emissions from your value chain to gain knowledge of your environmental impact and promote compliance with evolving regulations.
-   Create fiscal calendars to accommodate your organization’s unique fiscal calendar, providing the flexibility to collect and report data according to the defined fiscal calendars.
-   Use the emission factors content in the ESG content accelerator.
-   Enable ESG administrators to define either a simple approval flow or an advanced approval flow for all the metrics and metric definitions.
-   Address off-cycle requests to collect data for existing metric definitions and metrics by creating ad hoc metric data tasks on manual metrics.

 See [Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Model and prepare for potential outcomes with what-if scenario analysis tools that can help with your strategic planning.
-   Review the calculated metric definition data by using a formula tree so that you can access detailed information on the operands, metric definitions, metrics, and emission factors.
-   Streamline ESG metric tracking and enable trend analysis with enhanced Metric data tasks that support choice and HTML response formats and table improvements.
-   Import your historical metric data by using an import template to update and manage metric data within your organization.
-   Assign data owners dynamically for metrics that are based on configurations.

 See [Environmental, Social, and Governance Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Enable organizations to provide estimated data using pre-defined methods like average when actual data isn’t available.
-   Enhance data accuracy and governance by adding a review process for automated metric definitions.
-   Integrate real-time energy consumption data from DEX into the ESG Sustainable IT Dashboard for more accurate and reliable sustainability reporting, especially for desktops and laptops.
-   Enabled tracking and reusing narratives or statements for disclosures, making it easy to highlight specific achievements or commitments.
-   Enable creating claims directly from Microsoft Word to ServiceNow via the Microsoft 365 plugin.
-   Use enhanced entity-based access for metric definitions, metrics, metric data tasks, and metric data, enhancing data security and granular access control.
-   Create and synchronize claims automatically when uploading disclosures from Word via the ServiceNow add-in. This streamlines ESG reporting and confirming traceability across templates.
-   Avoid calculation inconsistencies caused by missing operand values. The Calculated Metric Definition Settings table enables specifying default values for operands, confirming smooth execution and flexible configuration.
-   When renaming a metric definition, there’s an option to apply the updated name to its child metrics and their associated metric data tasks.
-   Enabled audit tracking for emission factor tables and all changes are automatically logged for compliance and traceability.
-   Removed the unit restrictions between calculated metric definitions and emission factors, enabling any emission factor to be applied regardless of unit.

 See [Environmental, Social, and Governance Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

