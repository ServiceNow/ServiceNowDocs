---
title: Combined Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/delta-yokohama-australia/australia-yokohama-operationalsustainabilitymanagementformerlyenvironmentalsocialandgovernance-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Sustainability Management \(formerly Environmental, Social, and Governance\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

To use campaigns, activate the following system properties:

    -   sn\_esg.metric\_campaign: Enables campaigns on the Operational Sustainability Management workspace.
    -   sn\_esg.campaign\_bulk\_action\_enabled: Enables bulk submission, approval, and rejection for campaigns.
    -   sn\_esg.metric\_approval: Sets the approval mode for campaigns. Set the value to Simple for a single data owner and approver, or Advanced for multi-level approval chains.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Operational Sustainability Management \(formerly Environmental, Social, and Governance\).

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

</td></tr><tr><td>

Australia

</td><td>

-   **[Campaigns](https://www.servicenow.com/docs/access?context=campaigns&family=australia&ft:locale=en-US)**

After upgrading GRC: Metrics to version 22.5.2, you can group manual, calculated, and automated metrics into a campaign by entity, by group, or both. The unique combination of Group, Frequency, Calendar type, and Entity defines each campaign's metric set. When bulk actions are enabled, the campaign moves through different states as a single unit. Each measurement period generates a campaign cycle that tracks Data collection, Approval, and Closed states for every metric in the campaign together, instead of each metric progressing independently.


 -   **[Edit a calculated metric definition formula](https://www.servicenow.com/docs/access?context=edit-a-calculated-metric-definition-formula&family=australia&ft:locale=en-US)**

After upgrading GRC: Metrics to version 22.3.1, you can edit a calculated metric definition formula after it has been executed. When you save an edited formula, select a date from which the updated formula applies. Each saved edit creates a new formula version.

-   **[Microsoft Word based audit report templates using Document designer](https://www.servicenow.com/docs/access?context=document-designer-template&family=australia&ft:locale=en-US)**

After upgrading Document Designer to version 22.3.2, the Microsoft 365 reporting and Document Designer add-ins are consolidated into a single Document Designer plugin. A Create Claim button is added to the manifest. The repeater limit per document increases from 2 to 5, and the repetition limit per repeater increases from 200 to 500.

-   **[AI for document designer](https://www.servicenow.com/docs/access?context=ai-reporting-assistant&family=australia&ft:locale=en-US)**

With AI for Document Designer, you can use the AI reporting assistant to generate report content from ServiceNow data using prompts directly within Microsoft Word. The assistant inserts the output into your document as stories, tables, charts, or data points.

-   **[Components installed with Environmental, Social, and Governance Management \(formerly ESG Management\)](https://www.servicenow.com/docs/access?context=components-installed-with-esg&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.1, Operational Sustainability Management roles are mapped to Risk Library and Compliance Library feature roles to enforce functional domain separation. Users assigned these roles can access only risk and compliance records tagged to the functional domains they are authorized for.


 -   **[Configure data owner and approver assignments for a campaign](https://www.servicenow.com/docs/access?context=configure-data-owner-and-approver-assignments-for-a-campaign&family=australia&ft:locale=en-US)**

Configure data owner and approver assignments for a campaign from a single page. Submit, approve, or reject every task in a campaign cycle together instead of working through tasks one at a time.

-   **[Document intelligence for utility invoices](https://www.servicenow.com/docs/access?context=ai-driven-document-intelligence-for-utility-invoices&family=australia&ft:locale=en-US)**

After upgrading ServiceNow Otto for Operational Sustainability Management to version 22.0.1, unit values from invoices and updates metric data are extracted automatically, reducing manual data entry and improving data accuracy.

-   **[Integrating Environmental, Social, and Governance Management with Socialsuite](https://www.servicenow.com/docs/access?context=integrate-operational-sustainability-with-SocialSuite&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, streamline sustainability reporting and compliance processes by conducting CSRD-compliant double materiality assessments in Socialsuite and automatically syncing the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following Global Reporting Initiative \(GRI\) and European Sustainability Reporting Standards \(ESRS\) standards.

-   **[Create a threshold for a metric](https://www.servicenow.com/docs/access?context=create-a-threshold-for-a-metric&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, you can configure thresholds with multiple levels and ranges for granular monitoring. When thresholds are breached, automated actions trigger immediately.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features.

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

</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow Otto® name announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now Assist for IRM \(sn\_irm\_gen\_ai\) plugin, which provides generative AI capabilities for RCM, has been renamed to ServiceNow Otto for IRM.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Campaigns](https://www.servicenow.com/docs/access?context=campaigns&family=australia&ft:locale=en-US)**

The Campaigns list and record views were added to the Operational Sustainability Workspace. Related lists for entities, metrics, campaign tasks, owners, and approvers are included, along with declarative Add/Remove actions for managing campaign entities and metrics.


 -   **[Metric definition setting record fields](https://www.servicenow.com/docs/access?context=metric-definition-setting-record-fields&family=australia&ft:locale=en-US)**

After upgrading GRC: Metrics to version 22.5.2, Metric definitions now support a configurable variance base value, resolved from the individual metric, its metric definition, or a global default. Variance percentages remain meaningful when a previous-period value is missing or zero.


 -   **[Components installed](https://www.servicenow.com/docs/access?context=components-installed-with-grc&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.1, role inheritance is updated to restrict access only to the resources required for each role. These changes apply to new installations only.

    -   The connection\_admin role is removed from sn\_esg.integration\_admin inheritance.
    -   The workspace\_user role is removed from Formula Builder configuration table access and from sn\_esg.reader and sn\_esg.data\_owner inheritance.
    -   The sn\_align\_core.ap\_read\_only role in sn\_esg.reader is replaced with sn\_ppm.reader.
    -   Read access to the sn\_esg\_gen\_ai\_emission\_calculation\_guidelines table is restricted to sn\_esg\_gen\_ai.cmd\_agent\_user.
    -   Metric reader access to Sustainable IT tables is restricted to required configuration tables only.
-   **[Configure templates](https://www.servicenow.com/docs/access?context=configure-template-for-document-designer&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.2, the Business domain field in the Template configuration and Data relationship tables now references the GRC business domain \(sn\_grc\_business\_domain\). Previously, these fields referenced the M365 business domain.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Operational Sustainability Management \(formerly Environmental, Social, and Governance\).

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

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Operational Sustainability Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Operational Sustainability Management \(formerly Environmental, Social, and Governance\), such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

-   ServiceNow Otto is the new name for the Now Assist experience in Operational Sustainability Management. All Now Assist references have been updated to ServiceNow Otto.
-   You can group manual, calculated, and automated metrics into a campaign by entity, group, or both. When bulk actions are enabled, you can move an entire campaign through its lifecycle as a single unit, instead of tracking each metric independently.
-   Set a variance base value for a metric, so percentage-based threshold calculations stay meaningful even without prior-period data or if the previous value is zero.
-   Edit calculated metric definition formulas after execution and apply updated formulas from a specific date, preserving historical data integrity with formula versioning.
-   Use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word.
-   Perform CSRD-compliant double materiality assessments in Socialsuite and automatically sync the results with the Operational Sustainability Management application.

 See [Environmental, Social, and Governance Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/delta-yokohama-australia/rn-combined-intro.md)

