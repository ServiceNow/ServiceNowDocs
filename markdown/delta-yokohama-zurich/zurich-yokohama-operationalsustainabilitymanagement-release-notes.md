---
title: Combined Operational Sustainability Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Operational Sustainability Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-operationalsustainabilitymanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Operational Sustainability Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Operational Sustainability Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Sustainability Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Sustainability Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Operational Sustainability Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Forecast planning and analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&family=yokohama&ft:locale=en-US)**

Model and prepare for potential outcomes by using forecast planning analysis. With these tools, you can create, save, or visualize multiple scenarios.

-   **[Formula tree](https://www.servicenow.com/docs/access?context=reviewing-formula-tree&family=yokohama&ft:locale=en-US)**

Explore the calculated metric definitions by reviewing a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.

-   **[Historical metric data](https://www.servicenow.com/docs/access?context=importing-metric-data&family=yokohama&ft:locale=en-US)**

Import the historical metric data by using a pre-defined import template with instructions. With this process, you can update and manage the metric data within your organization and help to ensure that all data complies with the established business rules.

-   **[Dynamic filtering for Microsoft 365 for ServiceNow Reporting](https://www.servicenow.com/docs/access?context=add-related-fields-0365&family=yokohama&ft:locale=en-US)**

Filter the fields dynamically and set up dependencies by using related fields. In the Microsoft 365 add-in, you can configure fields so that cascading filters are supported dynamically. You can select a value in a field and have the related fields automatically update to show the relevant options. This process helps you to streamline data entry and improve efficiency.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Operational Sustainability Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Forecast planning and analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&family=yokohama&ft:locale=en-US)**

The forecast planning analysis module is now included in the List view of the Operational Sustainability Workspace.


 -   **[Result types](https://www.servicenow.com/docs/access?context=create-manual-metric-definition&family=yokohama&ft:locale=en-US)**

If you have the ESG manager \[sn\_esg.metric\_manager\] role, you can now configure either text, choice, or HTML format options for responses to qualitative metric data tasks that are related to manual metric definitions, including both initial and overridden responses. These options help you achieve more precision and detail in your data collection process.

-   **[Metric data table filters and side panel enhancements](https://www.servicenow.com/docs/access?context=metric-data-table&family=yokohama&ft:locale=en-US)**

If you have the ESG data owner \[sn\_esg.data\_owner\] role, you can now apply filters by using the filter menu and reject or approve tasks from the metric data table side panel. Data owners can now multi-submit and assign approvers to multi-approve or reject tasks, with the option to use choice and HTML response formats.

-   **[Data owner assignment types](https://www.servicenow.com/docs/access?context=create-manual-metric-definition&family=yokohama&ft:locale=en-US)**

If you have the ESG Manager \[sn\_esg.metric\_manager\] role, you can now configure the Data Owner Assignment type to be either simple or advanced for manual metric definitions. When you select the Simple option, the system assigns the specified Data Owner or Data Owner Group to the Metric Data Task. If you choose the Advanced assignment option, which is available with the GRC: Approver Configurator application, you can set custom configuration conditions, tables, or data owners to dynamically assign data owners.

-   **Table added to the GRC: Metrics application**

The following tables were added to the GRC: Metrics application:

    -   sn\_grc\_metric\_import\_job
    -   sn\_grc\_metric\_data\_import
    -   sn\_grc\_metric\_st\_import\_log
    -   sn\_grc\_metric\_st\_transform\_history
    -   sn\_grc\_metric\_import\_template
-   **Table added to the Unified content management application**

The sn\_esg\_content\_issb\_citation table was added to the Unified content management application.

-   **Table added to the Forecast planning analysis application**

The following tables were added to the Forecast planning analysis application:

    -   sn\_grc\_forecast\_analysis
    -   sn\_grc\_forecast\_context
    -   sn\_grc\_forecast\_data
    -   sn\_grc\_forecast\_parameter\_data
-   **Database view added to the Scope 3 emissions management application**

The sn\_esg\_scope3\_asset\_emissions database view was added to the Scope 3 emissions management application.

-   **Changes made to the sn\_grc\_metric\_data\_task table**

In the sn\_grc\_metric\_data\_task table, the job\_submitted, job\_errors, choice, overridden\_choice, html, and overridden\_html columns were added. The type="string" attribute was added to the state column.

-   **Changes made to the sn\_grc\_metric\_metric table**

In the sn\_grc\_metric\_metric table, the period\_date, data\_owner\_type, data\_owner, and data\_owner\_group columns were added. The type="string" attribute was added to the domain\_area column.

-   **Changes made to the sn\_grc\_metric\_parent\_data table**

In the sn\_grc\_metric\_parent\_data table, the formula\_operands columns, and html columns were added.

-   **Changes made to the sn\_grc\_metric\_base\_definiton table**

In the sn\_grc\_metric\_base\_definiton table, the formula\_tree, result\_type, choice\_table, choice\_field, choice\_condition, data\_owner\_assignment\_type, source columns were added. The type="string" attribute was added to the frequency column.

-   **Changes made to the sn\_grc\_metric\_data\_by\_entity table**

In the sn\_grc\_metric\_data\_by\_entity table, the html column was added.

-   **Attributes modified in the sn\_grc\_metric\_collector\_data table**

In the sn\_grc\_metric\_collector\_data table, the display="true" attribute was removed from the collector\_definition column.

-   **Attributes modified in the sn\_grc\_metric\_data\_process\_queue table**

In the sn\_grc\_metric\_data\_process\_queue table, the reference\_cascade\_rule="delete" attribute was added to the metric\_definition column.

-   **Attributes modified in the sn\_grc\_metric\_definition table**

In the sn\_grc\_metric\_definition table, the type="string" attribute was added to the type, method\_type columns.

-   **Changes made to the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table**

In the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table, the related\_fields column was added. The display="true" attribute was added to the field\_name column in the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table.

-   **System properties are added to the GRC: Metrics application**

The following properties were added to the GRC: Metrics application:

    -   com.glide.event\_manager.grc\_metrics\_queue.even.load.distribution.enabled
    -   com.glide.event\_manager.grc\_metrics\_queue.claim\_limit

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Operational Sustainability Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Operational Sustainability Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Business rules were deactivated and moved to common script include methods as part of GRC Metrics. For more information, see the KB article: [KB1734660](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3De92f82dd476a9610b8a4aa25126d4356).

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

-   **Activation information**

Install Operational Sustainability Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** Operational Sustainability Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Operational Sustainability Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Sustainability Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

