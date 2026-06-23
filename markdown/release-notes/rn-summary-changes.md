---
title: Changes to Yokohama features and products
description: Cumulative release notes summary on changes to Yokohama features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/rn-summary-changes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-13"
reading_time_minutes: 135
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Changes to Yokohama features and products

Cumulative release notes summary on changes to Yokohama features and products.

Existing  products were updated and changed in Yokohama. This includes the renaming of certain buttons or features.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/search-suggestions/search-suggestions-overview.md)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/search-preview-ui-new.md)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


-   **[Consumer-grade search experience for search portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/viewing-search-results-ais.md)**

The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/using-ais-next-experience-app.md)**

The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/create-facet-ais.md)**

Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/grouping-attachment-srch-results-ais.md)**

When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


</td></tr><tr><td>

API

</td><td>

<table id="table_x1g_1mc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/server-api-reference/PDFGenerationAPIBothAPI.md)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/server-api-reference/PDFGenerationAPIBothAPI.md)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table>|API|Endpoints|
|---|---------|
|[Attachment API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/c_AttachmentAPI.md)|POST /now/attachment/file: A new parameter, creation\_time, can be used to capture attachment creation times when the Now Mobile app is offline and the attachment is uploaded to a record at a later time.|

<table id="table_lcr_kmc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

V1.4

</td><td>

[LeadtoCashCore - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/server-api-reference/LeadToCashCoreAPI.md)

</td><td>

Enhanced the performance of the Commit Instance API to improve number generation for the number field:-   effect\(\): The **\_records\_count** return object is added to provide details about newly inserted records for a particular table, such as the table name and number of inserted records.
-   commitInstance\(\): A new additional parameter, useNumberGenerator, is added to optionally generate and apply sys\_ids to new table records in bulk.

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/server-api-reference/cloudrnr-TestGenerationAPI-scoped.md)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr></tbody>
</table><table id="table_a2z_4yf_zdc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Customer Service Management

</td><td>

v1.2

</td><td>

[openFrameAPI - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/c_openFrameAPI.md)

</td><td>

subscribe\(\): Added new events-   openframe\_wrap\_up\_submitted
-   openframe\_heart\_beat

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatTheme interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/cllent-mobile-api-reference/NowChatThemeColorsAndroidInterface.md)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebTheme interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/cllent-mobile-api-reference/NowWebThemeAndroidInterface.md)

</td><td>

Updated available web view UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/cllent-mobile-api-reference/NowChatThemeableiOSProtocol.md)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/cllent-mobile-api-reference/NowWebThemeableiOSProtocol.md)

</td><td>

Updated available web view UI color defaults.

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|ATF Test Generator and Cloud Runner|2.7.2|[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/server-api-reference/cloudrnr-TestGenerationAPI-scoped.md)|Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.|

<table id="table_nbf_qmc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Accounts Payable Operations

</td><td>

v2.0.0

</td><td>

[AP Invoice API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/ap-invoice-api.md)

</td><td>

Add properties supporting bill-to address information.-   POST /sn\_spend\_intg/ap\_invoice/cxml
-   POST /sn\_spend\_intg/ap\_invoice/json

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[Cloud Runner Test Generation - POST /now/sn\_atf\_tg/test\_generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/cloudrunner-testgeneration-api.md)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr><tr><td>

Order Management

</td><td>

v11.3.0

</td><td>

[Product Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md)

</td><td>

The **productSpecification** request parameter has changed from required to optional.-   PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}
-   PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}
-   POST /sn\_ind\_tmt\_orm/order/productOrder
-   POST /sn\_ind\_tmt\_orm/productorder

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/product-inventory-open-api.md)

</td><td>

The **productSpecification** request parameter has changed from required to optional. These endpoints now retrieve all product inventory records. In prior releases, product inventory records without a specified product specification weren't returned.-   POST /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product/\{id\}

</td></tr><tr><td>

Product Catalog

</td><td>

v14.1.0

</td><td>

[Product Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/rest-apis/product-catalog-open-api.md)

</td><td>

The ability to specify product bundles has been added to the following endpoints:-   GET /sn\_tmf\_api/ catalogmanagement/catalog
-   GET /sn\_tmf\_api/ catalogmanagement/catalog/\{id\}
-   GET /sn\_tmf\_api/ catalogmanagement/productOffering
-   GET /sn\_tmf\_api/ catalogmanagement/productOffering/\{id\}
-   PATCH /sn\_tmf\_api/ catalogmanagement/productOffering/\{id\}
-   POST /sn\_tmf\_api/ catalogmanagement/productOffering
-   GET /sn\_tmf\_api/ catalogmanagement/productSpecification
-   GET/sn\_tmf\_api/ catalogmanagement/productSpecification/\{id\}
-   PATCH /sn\_tmf\_api/ catalogmanagement/productSpecification/\{id\}
-   POST /sn\_tmf\_api/ catalogmanagement/productSpecification

</td></tr></tbody>
</table>

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)**
    -   Invoice line statuses are updated as:
        -   PO matching error to Mapping error
        -   PO matching completed to Mapping complete
        -   Matching error to Mapping error
        -   Review mapping

-   **[Invoice ingestion process when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/accounts-payable-operations/invoice-ingest-docintel-unavailable.md)**

Accounts Payable Operations integration with Document Intelligence enables AP admin to create invoice manually when DocIntel is down. The capture invoice details activity card displays the **Create invoice** option.


</td></tr><tr><td>

Adoption Services

</td><td>

-   **[Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/adoption-services/guided-setup.md)**

Assign and transfer Guided Setup tasks to relevant users, for execution. This capability requires admin roles.

Set Guided Setup steps as mandatory by disabling the skip action.

You can now run the Guided Setup player or builder multiple times.

Select the multi-run feature while you’re configuring and executing the tasks multiple times.


-   **[Help Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/adoption-services/help-center.md)**

Navigate to What's New within the Help Center panel across all experiences, including Core UI. Starting in the Yokohama release, configuration support for this new feature is available in classic and custom pages.

This feature isn’t supported for non-Polaris users.


-   **[Embedded Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/adoption-services/embedded-help.md)**

Import non-English content without overriding the last uploaded language content.


-   **[Guided Tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/adoption-services/guided-tours.md)**

Create, edit, or delete Guided Tours from any scoped application including ServiceNow AI Platform.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/ai-search-analytics-dashboard.md)**

The performance metrics, trends, and charts for this dashboard have been refreshed to offer a cleaner visual experience.


-   **[AI Search analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/ai-search-analytics-dashboard.md)**

The **Date range** interactive filter now enables you to access data from the last 180 days, rather than the last 90 days.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Agent Client Collector

</td><td>

-   **[Explore metrics with Metric Explorer independent of Agent Client Collector Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/metric-intelligence/agent-workspace-ops-intelligence.md)**

Starting in version 4.1.0, view and monitor metric data with Metric Explorer, even if you have not installed Agent Client Collector Monitoring.

-   ****

Starting in version 1.1.0, ACC for Visibility has been renamed as Kubernetes Visibility Agent and consists only of what is currently CNO for Visibility. The term CNO for Visibility has been deprecated and replaced with Kubernetes Visibility Agent. All other ACC for Visibility functions are now part of Agent Client Collector for Visibility - Content.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Form template enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-workspace-form-templates.md)**

Use the following form template enhancements to create or edit templates as needed:

    -   The **Templates** tab in the configurable side panel displays larger template cards with the template name and an expanded description. Users can view different lists of templates, mark their favorites, and sort templates either alphabetically or by last used.
    -   The template form displays template fields in a clearly labeled form section and displays the line numbers and headings for each template line to improve readability
    -   The template tab header displays "Edit template" when a user opens a template in edit mode.
-   **[Front-line case page integration with knowledge guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md)**

Enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.

-   **[Resurface special handling notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/c_OnScreenAlerts.md)**

Display the special handling notes for a case at any time by selecting **Special handling notes** from the More actions menu on the case record action bar.

-   **[Customer Central application moved from family to store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/customer-central.md)**

Starting with the Yokohama release, the Customer Central application \(com.sn\_csm\_customer\_central\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Central store app.

-   **[Customer Activity Guided Setup now accessible from a new location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/configure-customer-activity.md)**

Use the following updates in Guided Setup to enhance navigation and access customer history configurations:

    -   Access the Customer Activity Guided Setup from **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   View Activity Contexts, Activity Types, Activity Groups, and Activity Type Templates within Guided Setup. You can also access them in the menu by navigating to **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   Customer Activity has been renamed to Customer History, maintaining the same functionality.
    -   Access the Business Rule in the Activity Feed where it is now listed independently alongside Activity Types, Activity Groups, and Activity Type Templates for improved accessibility. Previously, it was nested under Activity Types.
-   **[Front-line case page lookup component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md#section_dnl_3f4_s1c)**

The Front-line case page includes the following enhancements:

    -   Includes the Consumer lookup component.
    -   Uses advanced search to look up contacts and consumers.
    -   Contact and consumer record cards can be collapsed to display more record space.
-   **[Action bar layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md#section_imv_qhs_mbc)**

The following interaction record pages include an action bar with a single action layout:

    -   CSM Interaction record page
    -   CSM voice interaction record page
-   **[Comment and Work note modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md#section_gzj_wlb_s2c)**

Create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case record. Automatically display a modeless dialog that includes the content from the form template and then post that content to the activity stream.

-   **[Front-line case page contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md#section_trg_ypr_m1c)**

The Record Information tab in the contextual side panel includes the Overview and Active SLA cards. The contact card and timeline card have been removed to improve the page load time.

-   **[Recommended Actions AI search replaces Agent Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md#section_trg_ypr_m1c)**

Recommended Actions AI search replaces Agent Assist in the contextual side panel for the following record pages included with the CSM Configurable Workspace:

    -   CSM default record page
    -   Front-line case page
    -   CSM Interaction record page \(for type = Chat, Video, Walkup, Email\)
-   **[Customer History component features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/customer-history-component-features.md)**

Use the following features to provide agents real-time updates and customer history details:

    -   Automatically refresh the Customer History component when account, contact, or consumer details change.
    -   Prompt agents to add missing account or contact details instead of leaving fields empty.
    -   Display an empty component until an agent links a contact using the lookup component, then show the contact's details.
    -   Enables agent to view updated customer information directly in Customer History on the Front-line Case page.

</td></tr><tr><td>

Application Manager

</td><td>

-   **[Unlicensed application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/application-manager/available-for-you-app-mgr.md)**

In addition to details about applications that are already licensed, the "Available for you" tab of the Application Manager now includes information about applications that haven't been procured from the ServiceNow Store yet.


</td></tr><tr><td>

Audit Management

</td><td>

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The Audit Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Multi-factor Authentication enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/authentication/mfa-enforcement.md)**

MFA is mandated and is enforced to all the non-SSO login users accessing ServiceNow®.


</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[Using latest assessment template for conducting BIAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/using-smart-asmt-template.md)**

You can use the latest assessment template to conduct the Business Impact Analysis \(BIA\).


</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Process mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/process-mining/process-config-builder.md)**

Use the process mining enhancements to improve processes as needed:

    -   Removed the viewer role from all records in the Process Mining Content Pack for Customer Service Management \(CSM\).
    -   Set process configurations as read-only templates, deletable only by a process mining administrator. You can enable customers to copy the template or import specific parts into their custom configuration.
-   **[Case lines and workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/case-line-form.md)**

The Case Line table \(sn\_case\_line\) includes the **Install base** and **Asset** reference fields. These fields display information based on the selected account and product.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Enhancements to the guardrails check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/servicenow-ai-platform-security/cse-ppi-config.md)**

The Code Signing Guardrails check has been improved to enhance signature verification, resulting in more secure workflows. In addition, multiple optimizations have been implemented to improve the performance benchmarks of the Guardrails scan, and log files now feature a more intuitive naming convention, which simplifies file identification within your system.


-   **[Generate update sets with a maximum size of 10,000 records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/servicenow-ai-platform-security/cse-turn-on-cse.md)**

Code Signing now enforces limits on large update sets to improve the user experience. The maximum size for an update set is 10,000 records.


-   **[Naming updates for trusted and production instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/servicenow-ai-platform-security/code-signing-landing.md)**

The trusted non-production instance has been renamed to trusted instance, and the protected production instance has been renamed to protected instance. These naming updates have been made to better align with customer usage.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[Improved user experience for adding hyperlinks in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/collaborative-work-management/cwm-docs.md)**

Insert hyperlinks in a Doc easily and quickly through the formatting toolbar, inline commands, or by pasting a copied link. The pasted URL can be converted into a hyperlink by pressing the Space or Enter key and edited using the inline edit modal.

-   **[Improved user experience for copying links of Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/collaborative-work-management/board-views-in-cwm.md)**

Ensure that your team sees the same data as you while sharing links of your Boards through the **Copy link** action, which now accesses the linked workspace showing the view in which the Board is displayed to you regardless of the user's view settings.

-   **[Redirection to the CWM task from notification emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/collaborative-work-management/cwm-boards.md)**

Access task details when you open a task from an assignment email from CWM in a new browser tab in the context of its Board rather than being directed to the workspace home page.

-   **[Redirection to the specific doc pages from notification emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/collaborative-work-management/cwm-docs.md)**

Access the specific Doc page that you are @-mentioned in by selecting **View Doc** in the notification email, eliminating the need to look through multiple pages in the Doc.

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The CWM workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Common Core

</td><td>

-   **[Column Organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-an-audit-report-template.md)**

You can select and reorder columns when adding a table into your template by using the Document designer Microsoft Word add-in. You can now organize your content better to meet your reporting needs.

-   **[Create content configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-common-functions/create-content-configurations.md)**

You can add up to 20 columns in a table and content block by using the Document designer application. You now have more flexibility with customizing your table and content block to meet your reporting needs.


-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Compliance Case Management

</td><td>

-   **[Roles updated for smart assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/compliance-case-management/roles-compliance-case-management.md)**

The following roles in Compliance Case Management have been updated with respect to smart assessments.

    -   sn\_comp\_case.compliance\_case\_admin
    -   sn\_comp\_case.compliance\_case\_analyst
    -   sn\_comp\_case.compliance\_case\_business\_user
    -   sn\_comp\_case.compliance\_case\_manager
-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The Compliance Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[Access changes for the sn\_cmdb\_editor and sn\_cmdb\_admin user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/installed-with-cmdb-workspace.md)**
    -   Starting with Yokohama Patch 4 \(zbooted or upgraded\), access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and the sn\_cmdb\_admin \(CMDB Admin\) user roles which are used in [CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md). The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Yokohama Patch 6 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

This scheduled job modifies user roles as follows:

        -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
        -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the 'Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles' scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).
-   **[CMDB Workspace v6.3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)**
    -   Apply the filters that were previously available only to the coverage charts to all charts in the Discovery sources tile in the CMDB 360 dashboard. For example, you can filter out non-CMDB tables or include records only from principal classes. For more information, see [CMDB 360 experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb360-exp-cmdb-workspace.md).
    -   Use a condition builder or a custom script to narrow down the list of de-duplication tasks that are assigned to a template. For more information, see [Create a de-duplication template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/workspc-dedup-create-template.md).
    -   Use the new **Allow empty field values** option to allow or disallow certification of empty value fields when creating a certification policy type in CMDB Data Manager. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/data-manager-create-policy-wrkspc.md).
-   **[CMDB Workspace v6.4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)**

You can now use dot-walking when setting assignments for the User Field or User Group Field options for CMDB Data Manager policies \(such as Certification\). Also, when converting legacy certification schedules into Data Manager Certification policies, existing dot-walking settings are preserved. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/data-manager-create-policy-wrkspc.md).

-   **[CMDB Workspace v7.4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)**

In the CMDB Workspace version 7.4, you can now do the following tasks:

    -   Manually create a CI in CMDB Workspace that complies with its class identification rule and other class requirements, and is tested for uniqueness in CMDB, to help ensure that the CI is valid and maintains the integrity of CMDB. For more information, see [Create a CI manually in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/create-ci-manual-cmdb-workspace.md).
    -   Set the CMDB Health dashboard to use the legacy methods to calculate the completeness, correctness, and compliance KPIs. That legacy calculation method relies on settings of proportional weights of metrics within the aggregated score of KPIs and was used up until the Washington DC release. By default, those weights aren’t used in the calculations of KPI scores.

Also, the CMDB Health dashboard now shows the overall score, which by default, is a simple average of the aggregated scores of the completeness, correctness, and compliance KPIs.

-   **[CMDB Workspace v7.5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)**

In the CMDB Workspace version 7.5, you can now do the following tasks:

    -   Delete CMDB Data Manager retirement definitions in CMDB Workspace \(other than the cmdb\_ci retirement definition\). For more information, see [Delete a CMDB Data Manager retirement definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/data-manager-manage-ret-def-wrkspc.md).
    -   Configure a CMDB Data Manager certification policy to disallow reviewers, to update fields' value while reviewing CIs in a certification task. Administrators can clear the **Allow updates to field values** option to prevent reviewers from updating non-compliant field values into compliance, resulting in rejecting those CIs. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/data-manager-create-policy-wrkspc.md).
    -   Schedule a de-duplication template for daily, weekly, monthly, or periodic runs for continuous remediation of duplicate CIs. For more information, see [Schedule a de-duplication template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/workspc-dedup-schedule-template.md).
    -   Receive notifications from CMDB Data Manager about certification and attestation tasks, that are incomplete or overdue. For more information, see [Components related to CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/components-cmdb-data-manager.md).
    -   Review and process tasks of your direct reports and of members of any user group that you manage. For more information about accessing these tasks in CMDB Data Manager, see [My Work view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace-govern-view.md).
    -   Reject a CMDB Data Manager life-cycle task in CMDB Workspace. For more information, see [Review CMDB Data Manager tasks in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/data-manager-review-task-wrkspc.md).
    -   Use the Create CI experience with a preset class when drilling down a class in the CI Summary chart on the Home view of CMDB Workspace. For more information about creating CIs manually while applying IRE processes, see [Create a CI manually in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/create-ci-manual-cmdb-workspace.md).
-   **[Update to the Walk stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-walk-tab.md)**

The Technical Service Offerings with Support Group or Change Group report now includes data that meets the **sys\_class \_name = offering** parameter.

-   **[Table label changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md)**

The following table labels have changed:

    -   The label for the cmdb\_ci\_service\_auto table is now Service Instance instead of Application Service.
    -   The label for the cmdb\_ci\_service\_technical table is now Technology management service instead of Technical service.
-   **[Class descriptions showing in the user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md)**

The descriptions for the base system classes are now integrated into CI Class Manager and appear in the **Description** field, on the Basic Info page for a class.

-   **[Reflow for configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The CMDB configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[Generate the OSCAL SSP model of an authorization package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/generate-oscal-models.md)**

Export the SSP model of an authorization package in the OSCAL format. The exported report contains only the control objectives linked to the authorization package and their additional information, such as inherited controls and the hierarchy of the control objectives.

-   **[Generate ATO artifacts in Microsoft Word and HTML templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/generate-ato-artifacts-cam-ws.md)**

Use the Document designer plugin \(com.sn\_grc\_doc\_design\) to create report templates in Microsoft Word. A new property module has been introduced to select the template type as a Microsoft Word template in addition to an HTML template.


</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Select contract type while initiating a third-party contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-initiate-non-ss-cnt.md)**

In the Initiate contract window, the **Type** field appears when you select the **Third party paper** option. You can specify whether the contract request is for a single contract or multiple contracts.

If you select **Single contract**, a **Contract type** field appears where you can define the type of contract document. This field isn’t available when you select **Multiple contracts**.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/legal-service-delivery/snlc-submit-request-tpc.md)**

When you're creating a third-party contract review request from Employee Portal, you can now select a single contract document to classify it as a single contract type. By selecting multiple contract documents, you can classify them as a multiple contracts type. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-add-clauses-doc-tmplt.md)**

You can now define the clause conditions on the fields and variables of a table that isn’t directly linked to the contract template table. The **Advanced script** check box in the Clause Variation form enables you to add custom logic to determine when a clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-append-data-table.md)**

You can now use scripts to insert additional data from the related table fields into the dynamic tables of a contract. The **Advanced script** check box in the Column Mapping form enables you to configure dynamic tables in a contract template to display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-create-ct-word-addin.md)**

You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

**Note:** To avoid configuration issues, ensure that you select the same table across all related configurations.

-   **[Configure dynamic tables for contract template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-addin-table.md)**

You can now set up the contract template on the Contract Request \[sn\_cm\_core\_contract\_request\] table. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

Additionally, the **Table** field has been renamed to **Lookup table** where you can select the table from the data that is populated into the contract document.

If the template isn’t based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Signature blocks enabled by default for new contract templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-create-ct-word-addin.md)**

When you’re creating a contract template, the **Signature blocks** check box in the Word Template New Record form is selected by default. If you want to configure the participant-based signatories for the contract template, you can clear the check box.

-   **[Copy fields from parent request to contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-copy-fld-frm-parent.md)**

You can now configure the ContractManagementExt extension point to automatically copy the required fields from the originating business unit record to the contract request when it’s initiated.

-   **[Modify signatories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-pause-signature.md)**

Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md)**

The wet signature process has been enhanced for better control and clarity. Wet signature requests are sent one signatory at a time, starting with the first signatory in order. When the signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Resend signature request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-resend-sign-req.md)**

Enable contract fulfillers to manually trigger a signature request when needed, instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configuring signatories in Contract template using Microsoft Word add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-config-sign-addin.md)**

Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\), instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.

-   **[Upload and parse a Microsoft Word document that includes content controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-upload-doc-addin.md)**

Upload the contract document directly from the Microsoft Word Add-in instead of selecting it from your system.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Playbooks use only published forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/creator-studio/creator-studio-add-automation.md)**

As of Creator Studio version 27.2.2, forms must now be published \(marked as ready\) before you can use them to create an automated playbook.

-   **[Hide the App Engine Studio template with a new system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/creator-studio/creator-studio-components-installed.md)**

As of Creator Studio version 27.2.2, Creator Studio users who have both App Engine Studio \(AES\) and Creator Studio installed will no longer see the AES template when they create an app. Admins can choose to show the AES template using the new **com.glide.creator\_studio.template\_deny\_list** system property.

-   **[Form location removed from form creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/creator-studio/creator-studio-edit-form-settings.md)**

Defining the catalogs and topics for a form is now accomplished by modifying the form settings rather than being done during the form creation process. If you haven't defined a location for a form, you are prompted to do so before you can mark it as ready.


</td></tr><tr><td>

Data Loss Prevention Incident Response

</td><td>

-   **[Create additional incident data fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/data-loss-prevention/create-custom-fields-dlp.md)**

In the DLP incident table, the **Custom Fields** column has been renamed **Additional Incident Data Fields**.


</td></tr><tr><td>

Data Management

</td><td>

-   **[Data Management Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/viewing-data-usage.md)**

You can now access data usage on your instance by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**.


</td></tr><tr><td>

Data management for CSM

</td><td>

-   **[Product Inventories configurations for Customer Life Cycle Management workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/product_inventory_configurations.md)**

Perform the Modify, Suspend, Resume, and Disconnect operations on product inventory records directly from the Product Inventory related list on the Accounts page.

-   **[Grant write access to account relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_CreateAcctRelationshipRecord.md)**

Enable administrators and customer service managers to update account relationship records.

-   **[Enable write access to contact relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_CreateAContactRelationship.md)**

Enable administrators and customer service managers to update the contact relationship records.

-   **[Populate the Type field in relationship tables using the fix script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/migration-of-account-manager-responsibility-access.md)**

Migrate the account manager responsibilities from the account team member relationships to the new responsibility access configurations. The updated framework enables you to manage access settings more efficiently.

-   **[Update roles within relationship agent and relationship contributor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/features-supp-and-unsupp-by-unified-consumer.md)**

Modify the roles of the relationship agent and relationship contributor to include the new granular roles that can grant access by responsibilities.

-   **[Notification for case tasks at business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/manage-business-location-cases.md)**

View the notifications for the case tasks that are associated with the business locations on the Business Location Service Portal \(BLSP\). This way, your location members can stay informed about their pending tasks.

-   **[Case resolution by location staff at other business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ebl-as-a-fulfiller.md)**

Enable your location staff, whether at company-owned or third-party-owned organizations \(internal and external business locations\), to handle and resolve issues from other eligible business locations.

-   **[Inbound Request Configuration table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/inbound-request-configuration-table.md)**

The Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table is renamed to Inbound Request table.

Use the **Request Configuration** field on the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to reference the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table while executing synchronous or asynchronous flows.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Simplified onboarding of orchestration tools not supported in the base system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/devops-user-created-orchestration-tool-integration.md)**

Integrate orchestration tools that aren’t supported in the base system by leveraging a generic framework.

-   **[Custom fields for planning tool integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/add-custom-field-for-a-planning-tool-integration.md)**

Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.

-   **[Additional scans for DevOps Health Scan Content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/run-health-scan-check.md)**

Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/devops-wkspc-bitbucket-tool-conn.md)**

Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/change-request-creation-with-devops-data-retrieval-errors.md)**

Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/create-devops-change-request-manual.md)**

Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/servicenow-devops-custom-actions-from-github-marketplace.md)**

The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/configure-webhooks-for-rally-manually.md)**

Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/servicenow-custom-actions-for-gitlab.md)**

The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/dev-ops-change-acceleration.md)**

Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/create-change-sow.md)**

View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/sc-github.md)**

The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/dev-ops-administration.md)**

Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/playbook-enter-github-instance-details.md)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/run-health-scan-check.md)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/sc-github.md)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/devops-reference-error-messages.md)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/installed-with-dev-ops.md)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/dev-ops-commits-release.md)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/dev-ops-config-change-details.md)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/config-dev-ops-extensions-azure.md)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/servicenow-custom-actions-for-gitlab.md)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/run-health-scan-check.md)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/devops-jfrog-connect-workspace.md)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/devops-jfrog-connect-workspace.md)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/servicenow-custom-actions-for-gitlab.md)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/run-health-scan-check.md)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/devops-change-velocity/dev-ops-change-acceleration.md)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/integration-hub/visa-spoke.md#section_gsl_nw5_vyb)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 25.2 revision changes.


</td></tr><tr><td>

Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-and-visual-insights-ai-agent.md)**

Generate a summary of document and image attachments with the document and visual insights AI agent.


</td></tr><tr><td>

Document Services

</td><td>

-   **[PDF generation and accessibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/document-management-services/pdf-generation-accessibility.md)**

Export a collection of records or a single record into a PDF format. New system property was added for better accessibility.

-   **[Workflow migration for Managed Documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/document-management-services/c_ManagedDocuments.md)**

Improved usability, low code accessibility, and feature parity due to the newly configured workflows.​

-   **[Subflows for Shared drives for Google Drive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/document-management-services/google-drive-spoke-document-services.md).**

Added Spoke subflows for Shared drives in Google Drive.

-   **Summarize button.**

The **Summarize** button was changed to the **Ask Now Assist** button.


</td></tr><tr><td>

ERP Semantic Mining

</td><td>

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **[Faster initialization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-customization-mining/how-erp-clean-core-inputs-data.md)**

In addition to daily total application statistics, the SQLM and APPSTATS initial scan now also retrieves all monthly total application statistics up to the current date.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Refresh flow in OT workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/enterprise-asset-management/request-eam-assetrefresh.md)**

For single and multi-model refresh orders, the OT manager can edit the replacement model even after the refresh order has been created in the OTAM workspace. Additionally, the sourcing location is also editable.

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The configurable Enterprise Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Property name changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/event-management/enable-alert-grouping.md)**

**Enable CMDB Correlation for Alert Aggregation \( CMDB groups\)** \(**sa\_analytics.agg.query\_cmdb\_correlation\_enabled**\) has been renamed **Enable CMDB correlation**.

**Enable alert aggregation for CI-based Automated groups** \(**sa\_analytics.specific\_patterns\_enabled**\) has been renamed **Enable ML based Automation correlation**.

**Enable alert aggregation for Text-based groups** \(**sa\_analytics.text\_based\_group\_enabled**\) has been renamed **Enable Text based correlation**.

**Use all CMDB relations for CMDB group correlation. This property impacts both CMDB group correlation and Alert Similarity on the Alert form** \(**evt\_mgmt.related\_cis\_get\_all\_relation\_types**\) has been renamed **Use all CMDB relations for CMDB group correlation**.

-   **[Pull connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/event-management/t_EMConfigureConnectorInstance.md)**

Simplifying the setup for Out-of-the-Box \(OOTB\) event rules that come with the pull connectors that have not yet been activated, deactivated, or modified, the Apply additional matching rules option is now enabled by default. If a rule has been previously applied, you must set this option manually.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/analytics-external-content-connectors.md)**

Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/create-ext-cont-connector-jira.md)**

The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/create-ext-cont-connector-microsoft-onedrive.md)**

The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/create-ext-cont-connector-mspo.md)**

The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/create-ext-cont-connector-msteams.md)**

The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/webcrawler-external-content-connector.md)**

The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which allows you to specify a custom web source or select a predefined one.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[SLAs in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/field-service-scheduling/using-dispatcher-workspace.md)**

The SLAs breached query on the Dispatcher Dashboard in Dispatcher Workspace has been updated to look at the SLAs that are associated with the work order tasks only instead of the work orders and work order tasks. The SLA breached counter on the task cards is also static, instead of real time. For more information on changing the SLA timer on task cards, see the Enable the **SLA timer on work order task cards** property on [Configure settings for Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/configure-workspce-settings.md).

-   **[Assignment groups and territories in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/field-service-scheduling/using-dispatcher-workspace.md)**

You must save the default assignment groups or territories in Dispatcher Workspace to load when you open Dispatcher Workspace. If you don’t have the defaults saved, then you must select the assignment groups or territories to appear every time you open Dispatcher Workspace. This change is made to improve the performance of Dispatcher Workspace. For more information on saving the default assignment groups, see the Groups section on the **General** tab on [Enable Dispatcher Workspace settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/field-service-scheduling/dispatcher-wrkspc-settings.md). For information on saving default territories, see [Select Territories in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/field-service-scheduling/select-territory-dispatch.md). Administrators can disable this by setting the **sn\_fsm\_disp\_wrkspc.enableEmptyState** system property to false.

-   **[Work order questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/work-order-management/complete-questionnaire-mobile-app.md)**

Availability of inline choices for a question and the ability to add additional information for a question when completing a work order questionnaire through the Now Mobile Agent application.

-   **Role to access opportunities**

The Opportunity Writer sn\_opty\_mgmt\_core.opportunity\_writer role has been replaced with the Opportunity Contributor sn\_opty\_mgmt\_core.opportunity\_contributor role. Field service technicians can use the new Opportunity Contributor\[sn\_opty\_mgmt\_core.opportunity\_contributor role to create and view opportunities.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/financial-services-card-operations/card-operations-reference.md)**

Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **[Added fields to Claim Base table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/financial-services/fso-core-insurance-tables.md)**

Added the following fields to the Claim Base \[sn\_bom\_claim\_base\] table:

    -   SIU review
    -   Claim validation decision
    -   Claim fraud decision

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/financial-services/components-installed-with-the-financial-services-operations-integration-with-visa.md)**

Updated the following subflows to align with release 25.1 revision changes:

    -   Submit Dispute questionnaire
    -   Submit fraud report

</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Configure Data Privacy and Data Discovery to protect the personally identifying information \(PII\) of your users.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/data-privacy-classic/configure-now-assist-data-privacy.md)**

Generative AI Controller has changed to use the Data Privacy application instead of the Sensitive Data Handler to help anonymize PII. The process for choosing what gets anonymized and how has shifted to different tables and forms that your administrator must configure for your organization.


</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The configurable Hardware Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **[Component-based alert grouping is deprecated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md)**

Starting in version 36.0.19, the adoption of a streamlined two-tier alert model, Log Analytics Group to Single Alert, has replaced component-based alert groups, which have been removed. This model aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[Enrich automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/service-operations-workspace-for-itom-apps/enrich-alert-sow-itom.md)**

Introduced a new section **And finally** that contains two radio buttons that replace the previous **Continue running automations of this type** toggle switch.

    -   **Run other enrich alert automations** continues running automations with the same filter conditions.
    -   **Don't run other enrich alert automations** halts additional automations after execution, except those owned by other assignment groups.
-   **[Investigate alerts using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-for-it-operations-management/nai-past-incidents.md)**

Investigate alerts using Now Assist, which now uses the Retrieval-Augmented Generation \(RAG\) process to enhance alert investigation. This enhancement enables the retrieval of highly relevant past incidents, providing accurate context and actionable insights. Now Assist also notifies users of those involved in past or present efforts to resolve similar issues, promoting collaboration and reducing duplicated efforts.

-   **[Component-based alert grouping is deprecated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md)**

Starting in version 36.0.19, component-based alert groups are removed as Health Log Analytics adopts a streamlined, two-tier alert model: Log Analytics Group to Single Alert. It aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   **[Cloud Services Catalog Terraform Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/cloud-configuration-governance/cpg-terraform-connector-landing-page.md)**

Cloud Provisioning and Governance: Terraform Connector has been renamed Cloud Services Catalog Terraform Connector


</td></tr><tr><td>

ITOM Optimization

</td><td>

-   ****
    -   Migration of legacy workflows to Workflow Studio flows or subflows.
    -   Policy Rule Actions now supports Workflow Studio subflows instead of legacy workflows.

</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Name suggestions for application service candidates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/service-mapping/app-services-name-suggestions.md)**

Experience more accurate name suggestions for application service candidates based on Service Fingerprints in Service Mapping Plus store version 1.15.0.

-   **[Limits in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/service-mapping/components-installed-with-service-mapping.md)**

Limits in Service Mapping prevent the disabling or deletion of jobs scheduled for the Checkpoint Reaper or the Service Model's Blob Reaper.

-   **[Limits in tag-based Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/service-mapping/components-installed-with-service-mapping-plus.md)**

Starting with version 1.15.2, experience improved performance in Service Mapping. A new property limits the creation of tag-based service candidates to 200 per service family.

-   **[Name update in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/create-it-services.md)**
    -   Application Services in the navigation menu has been renamed Service Instances.
    -   The label for the \[cmdb\_ci\_service\_auto\] table has been changed from Application Service to Service Instance.
-   **[Discovery status monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/discovery/c_DiscoveryStatus.md)**

Discovery schedules that have no status updates for over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items.


</td></tr><tr><td>

Identity

</td><td>

 

</td></tr><tr><td>

Impact

</td><td>

-   **New [Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-store-app.md) experience**

The new Impact Store Application provides a more efficient, streamlined way for you to work. For information about how to upgrade, see [Configuring the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/configuring-impact-platform.md). Note that [Impact Delivery Instance \(formerly Impact Digital Experience\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-digital-experience.md) is still supported in this release.

-   **[Value Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-value-journey.md) name changes:**
    -   Impact Value Journey is renamed to Impact Value
    -   Value Blueprint is renamed to Objectives and Outcomes.
    -   Outcomes Performance is renamed to Outcomes Insights.
    -   Business Objectives is renamed to Objectives.
    -   Operational Outcomes is renamed to Outcomes.
    -   Business Value Report is renamed to Value Report.
-   **[Impact Workspace name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-in-platform-home.md)**

Impact Workspace has been renamed as Impact.

-   **[Impact Store App user experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-store-app.md)**

Impact users who have migrated from the Impact Delivery Instance may access Quicklinks to access features that haven’t been migrated to Impact Store Application yet.

-   **[Custom payload in Instance Observer alerts integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/custom-payload-help-guide-impact.md)**

Define and manage a custom JSON request payload for ServiceNow and third-party integrations with the Instance Observer enhancements.

-   **[Accelerator catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/accelerator-catalog.md)**

Minor updates have been incorporated into the following accelerators:

    -   [Jumpstart Your GenAI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-gen-ai.md)
    -   [Jumpstart Your Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-now-assist-skill-kit.md)
    -   [Jumpstart Your Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-document-intelligence.md)
    -   [On-Demand Value Report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/on-demand-value-report.md)
    -   [LSD Maturity Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/lsd-maturity-assessment.md)
The following Accelerators are renamed:

    -   Jumpstart Your Now Assist for ITSM is now [Jumpstart Your AI Agents for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-your-ai-agents-for-itsm.md)
    -   Jumpstart Your Now Assist for CSM is now [Jumpstart Your AI Agents for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/accelerator-and-initiative-list/jumpstart-ai-agents-csm.md)
-   **[Impact packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-packages.md)**
    -   Add-on SKUs have been updated to provide additional flexibility for Impact customers and are available in all environments where Impact is available.
    -   Updates to the Impact Advanced package, offered pursuant to the applicable Impact Accelerator Description available at  [https://www.servicenow.com/legal/servicenow-impact.html](https://www.servicenow.com/legal/servicenow-impact.html).
-   **[Data Collection Toolkit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/value-library/data-collection-toolkit.md)**
    -   Download the content packs for both regulated \(GCC/NSC\) and non-regulated customers.
    -   Automatically transfer Impact Value Metrics to the centralized Impact instance to manage the value journey, including setting value baselines and targets, outcome performance reviews, and the value report with the enhanced toolkit.
-   **[Impact Delivery Instance \(formerly Impact Digital Experience\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/impact/impact-digital-experience.md)**

With the Yokohama release, Impact Digital Experience \(IDE\) has been renamed as Impact Delivery Instance \(IDI\).


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Email redirection behavior for major incident email notification links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/incident-management/email-notif-redirt-inci-major-inci.md)**

In major incident email notifications, you can now decide where the links to a major incident record are redirected. Instead of a major incident record automatically opening in the classic UI16 interface in Major Incident Management, the record can be opened in SOW. The major incident record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including major incident.
    -   The **Redirect SOW Email notification for Major Incident Management** \(**sn\_major\_inc\_mgmt.sow\_email\_notification\_redirect.mim**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Email redirection behavior for incident email notification links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/incident-management/email-notif-redirt-inci-major-inci.md)**

In incident email notifications, you can now decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the classic UI16 interface in Incident Management, the record can be opened in SOW. The incident record link in an email notification opens in SOW only if you have the sn\_sow\_user role and any of the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including incident.
    -   The **Redirect SOW Email notification for Incident Management** \(**sow\_email\_notification\_redirect.incident**\) property is set to `true`. You can create this property if you want to enable or restrict the email redirection behavior specifically for the incident table. This property, if created and set, overrides the **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) base system property.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

To ensure consistency, the email notification templates for incident tasks are also updated to send the notification from Service Operations Workspace \(SOW\) in the same format as sent from classic UI16 interface similar to incident. Also, the template theme is updated to match the Next Experience theme.

-   **[Incident and problem workflow changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/incident-management/incident-management-properties.md)**

When a problem is fixed and the **Share fix** option is triggered, the event is added to the **Work notes \(Private\)** field instead of the **Additional comments \(Customer visible\)** field for the incident associated with the problem record.

This feature is available in the base system for the new customers. For existing or upgrade customers, admin must set the **Communicate problem workaround to incident worknotes** \(**com.snc.incident.communicate\_prb\_workaround\_to\_inc\_worknotes**\) system property to `true` to enable the feature.

-   **[Changes in the reopening incident behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/incident-management/reopening-incident.md)**

Enable the agents with incident write access, callers, requesters, or **Opened by** end users to reopen a resolved incident. Both the caller and the requester can view and use the **Reopen** option on the incident classic UI16 form and the Portal UIs, such as Service Portal and Employee Service Center \(ESC\) portal.

An agent can view and use the **Reopen** option on the incident classic UI16 form to reopen any incident that is assigned to them or to other agents. However, on the Portal UI, an agent can only view and use the **Reopen** option to reopen an incident if it’s assigned to them.

-   **[Sorting CIs in incident forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/incident-management/create-an-incident.md)**

The search performance of the available CIs for the **Configuration item** field on an incident form is enhanced to promote a clean UI and quick loading and sorting of the CIs. The search results that list the CIs are sorted alphabetically by CI name instead of by CI class and then CI name. The **ref\_ac\_order\_by=sys\_class\_name** attribute is removed from the default attributes on the **cmdb\_ci** field of the Task \[task\] table, which increases the performance of the field.

This change is applicable to new and existing users using the default attributes. You can use the **Override attributes** option to restrict this change for any required child tables that extend to the **cmdb\_ci** field of the Task \[task\] table.


</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Viewing multiple records at once in the Equipment Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/industrial-process-manager/managing-equipment-models-after-data-import.md)**

In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


</td></tr><tr><td>

Instance Data Replication

</td><td>

-   **[Seeding request improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/instance-data-replication-idr/exploring-instance-data-replication.md)**

In V2 replication sets, the number of records in a seeding request is now unlimited.

-   **[Data comparison improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/instance-data-replication-idr/comparing-replicated-data.md)**

In V2 replication sets, the number of records in comparison or reseeding counts is now unlimited.

-   **[Reseed missing attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/instance-data-replication-idr/comparing-replicated-data.md)**

Attachments are now included in data comparison requests.

-   **[Seeding performance improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/instance-data-replication-idr/seed-consumer-instance.md)**

Seeding throughput and message queue efficiency has been optimized in IDR.


</td></tr><tr><td>

Insurance Claims Core

</td><td>

-   **[Added fields to Claim Incident table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/financial-services/insurance-claims-core-tables.md)**

Added the following fields to the Claim Incident \[sn\_ins\_claim\_property\] table:

    -   Injured
    -   Insured property

</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

MID Server

</td><td>

-   **[MID Server supports and requires a minimum JRE version 17](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md)**

The MID Server is compiled using Java 17 and is incompatible with any Java version below 17 for runtime execution. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10. See the [MID Server JRE Minimum Version Requirement Update to JRE 17 Starting from Yokohama Release \[KB1704368\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704368) article in the Now Support Knowledge Base for information about required procedures before upgrading the instance.

-   **[Improvements when manually installing a MID Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md)**

The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Input form screen enhancement and changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/parameter-input-screen.md)**

Use the following enhancements added to the input form screen:

    -   Selecting input values directly within the input form screen, either from a list or from a group of chips. Now users don’t need to navigate to a separate dedicated screen for value selection, when using the inline choice chips layout. You can also define the number of input values to display on an input form screen section.
    -   Ability to add images, plain text, and rich text within specific inputs. These added descriptive elements provide more context to your users and give a clearer idea of what is required for certain inputs. For example, an image can accompany a checklist to ensure that a piece of hardware is wired correctly.
    -   Provide users with the ability to perform actions in relation to the displayed input parameter, while working directly on an input form screen. The available actions are: navigate to another screen, add an attachment from the gallery or camera, and add a comment to a field. Users submit these added actions either when saving their progress or completing the input form screen.
    -   Save input form screen data before it's submitted. Users with access to the same record can see each other's changes either when saving their progress or completing the input form screen.
    -   Interact and switch between other navigation tabs while also working on the input form screen.
    -   Sections are no longer displayed if they don’t contain any input fields.
-   **[Additional number attributes for input form screens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/parameter-screen-var-attr.md)**

Use the following number attributes in your input form screens:

    -   Use the **CustomErrorMessage** attribute to specify an error message when a UI rule condition is met.
    -   Use the **SkipValidationWhenHidden** attribute to skip validation on hidden inputs.
-   **[Enable barcode scanning with an external scanner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/enable-external-barcode-scanner.md)**

Configure barcode scanning with an external scanner without denying access to the camera for the entire mobile app.

-   **[Mobile Publishing enhancements and changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/mobile-publishing.md)**
    -   Enabled Android deep links for multiple instances.
    -   Enhanced validation for transparent images used in branded apps.
    -   Support for public-facing screens in branded mobile apps. Admins can configure URLs that link to public-facing web pages. These web pages are displayed to end users without needing to log in to the mobile app.
-   **[Turn off Zero Trust Access banners in mobile app screens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/turn-off-zta-banner.md)**

In mobile client versions 19.4 and later, you can turn off Zero Trust Access banners on mobile screens. Turning off these banners can enhance usability of your mobile apps because the banner does not display each time the connection state changes so end users are not interrupted by the banner display. You can configure this behavior by setting the **disableZTABanner** mobile property on your ServiceNow instance.


</td></tr><tr><td>

Next Experience

</td><td>

-   **[Next Experience preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/set-up-preferences-next-experience.md)**

The new user preference panel provides a more efficient, streamlined way for you to work. Use the new search bar to locate your preferences. A wider modal displays all preference groups and when you select a group, all the individual preferences that are related to it appear in the same window.


</td></tr><tr><td>

Next Experience Components

</td><td>

<table id="table_qvp_xdg_zcd"><thead><tr><th>

Component

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

-   Select multiple slots
-   Add customizable categories for appointment slots
-   Hide past and unavailable slots
-   Add contextual tags in appointment slots
-   Configure number of rows displayed in each slot in the Day and DAYMOBILE views
-   Configure container height adjustment

</td></tr><tr><td>

Attachments

</td><td>

-   Option to download all attachments
-   Revised delete attachment confirmation popup message

</td></tr><tr><td>

Avatar

</td><td>

Configure avatar to behave as a button or a link.

</td></tr><tr><td>

Calendar

</td><td>

-   DST support with multiple time zones in the Calendar and Timeline views
-   Hide header
-   Multiple time zones in the Timeline view
-   Scroll control for the Calendar and Timeline views

</td></tr><tr><td>

Email composer

</td><td>

Now Assist generative AI suggestions for all email scenarios, email templates, response templates, and quick messages.

</td></tr><tr><td>

Email composer \(mini\)

</td><td>

Now Assist generative AI suggestions for all email scenarios, email templates, response templates, and quick messages.

</td></tr><tr><td>

Form

</td><td>

-   Configuration panel updates
-   Form controller configuration panel updates

</td></tr><tr><td>

Form templates

</td><td>

-   Sort templates alphabetically and by last used.
-   New tab for Favorites for you to add and remove templates.
-   Larger cards that don't truncate template name and description, and show Last used timestamp.

</td></tr><tr><td>

Highlighted value

</td><td>

-   Medium size variant.
-   Custom tooltip property.

</td></tr><tr><td>

iFrame

</td><td>

Send messages to iframed document.

</td></tr><tr><td>

Kanban Board

</td><td>

-   Multi-select in cards
-   Configure selecting dependency lines
-   Add secondary header

</td></tr><tr><td>

Modeless dialog

</td><td>

Make the dialog dynamic and automatically resize to fit the content.

</td></tr><tr><td>

Node Map

</td><td>

-   Force layout for representing graphs without structure or hierarchy
-   Custom popover configuration in Hierarchical, Layered, and Force layouts
-   Customizable nodes in non-unified layouts
-   Self-referencing nodes denoted with edges looping back to the node
-   Export maps in JPG and PNG
-   Aggregate or segregate multiple connections between the same nodes

</td></tr><tr><td>

Pill

</td><td>

Display the selected pill state which doesn't display by default.

</td></tr><tr><td>

Quick filter

</td><td>

-   Configure section headers in typeahead dropdown
-   Configure footer action button
-   Configure placeholder text value for input field

</td></tr><tr><td>

Record lookup

</td><td>

-   Search for contacts by name, phone, or email
-   Preview shortlisted results in a paginated form
-   Quickly link or unlink a shortlisted contact to a case
-   Edit details for a record without accessing the parent record
-   Hide record header
-   Configure search results
-   Render highlighted values in the linked card
-   Qualify search results using specific conditions \(reference qualifiers\)
-   Hide fields with empty values
-   Hide link button
-   Expand or collapse card

</td></tr><tr><td>

Stepper

</td><td>

-   Standardized font size \(small or medium\) for all steps
-   By default, pagination adjusts to display the current selected step

</td></tr></tbody>
</table><table id="table_eqq_1fg_zch"><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Bar

</td><td>

Percent \(%\) information added to chart tooltips and data table below chart.

</td></tr><tr><td>

Bubble

</td><td>

Percent \(%\) information added to chart tooltips.

</td></tr><tr><td>

Geomap

</td><td>

Percent \(%\) information added to chart tooltips and data table below chart.

</td></tr><tr><td>

Heatmap

</td><td>

-   Percent \(%\) information added to chart tooltips and data table below chart.
-   When the metric value is set to "Count," show a zero \(0\) when no data is available.

</td></tr><tr><td>

Pivot table

</td><td>

-   When there's no value in the selected dataset or for the configuration, choose the display format.
-   Data sources limit increased from 10 to 15.

</td></tr><tr><td>

Time series

</td><td>

-   Percent \(%\) information added to chart tooltips and data table below chart.
-   Support for business calendars such as Gregorian, fiscal, and any manually added calendar.
-   For all chart formats, except "column:"
    -   When there's no value in the selected dataset or for the configuration, choose the display format.
    -   For table data sources, when there's no data for a specific time on the chart, show a continuous line without gaps.
-   Show a chart and graph data table for easier screen reader access.
-   For line, spline, area, and step charts, have a marker show at each data point on the chart including where values are zero \(0\) or missing.
-   For a chart with up to 3 metrics, you can add alternative Group by's for each metric for the user to select from.
-   Sorting when data is grouped.
-   New Date range option to set the period end date to update automatically to the current date.

</td></tr></tbody>
</table><table id="table_y2f_x1z_4dc"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dashboards

</td><td>

-   Pills at the top of the page display any categories assigned to the dashboard
-   User avatars at the top of the page indicate real-time editing

</td></tr></tbody>
</table><table id="table_cr1_bfg_zce"><thead><tr><th>

Bundle

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Record list

</td><td>

-   Condition builder available in the list header
-   If live list is enabled, infinite scrolling is enabled by default

</td></tr></tbody>
</table>

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   **Time filters for events**

Icons were added to each event to enable you to select a timeframe when filtering events.

-   **Subtree filters for events**

Scroll and search through a selected portion of the component tree.


-   **Filters for traces**

Filter traces with front-end filters to streamline span visualizations, specialty filters to view targeted waterfall analysis without losing overall context, and level filters to adjust the detail display in span visualizations.


</td></tr><tr><td>

Notifications

</td><td>

-   **[Advanced filters in notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/advanced-notification-prefrences.md)**

Use notifications filters for categories, delivery channels, active or inactive notifications, subscriptions, and digest enabled notifications.

-   **[Support for assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/create-add-assignment-group.md)**

Send provider notifications for assignment groups and to users that are part of groups stored in sys\_user\_group table.

-   **[Advanced condition for provider framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/noti-new-update-notification.md)**

Use an advanced condition to send a notification that is based on the current email record, changing field values, or system properties.

-   **[Mandatory notifications for provider framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/make-notification-mandatory-provider.md)**

Make critical notifications mandatory for the provider framework.

-   **[Email bounce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/email-bounce.md)**

Prevent resending bounced emails to the addresses that are known to generate bounces.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

Enable translation settings is now Multilingual service in Now Assist admin console.

-   **[Default email client for email recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md)**

The Seismic email client is enabled by default on Core UI with the activation of email recommendation. This client provides the Generative AI application features for creating email responses, draft management, and template management.

-   **[Now Assist panel response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md)Now Assist panel response**

With the carousel experience removed, the Now Assist panel now generates a synthesized response for any user inquiry. This response includes content from Knowledge articles, flows &amp; actions, skills, and links to those articles, instead of only the Now Assist panel skills.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Platform Request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/ticket-status-aia.md)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Configuring Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/configuring-ai-agents.md)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Add a Knowledge Graph to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/add-knowledge-graph.md)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


[Yokohama Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8.md)

-   **[Confirm your web search tool provider data policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/add-web-search-ai-agent.md)**

If you select Google as your web search provider for web search AI agent tools, Google will use [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/version-control.md)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/add-tool-aia.md)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool from scratch. After an existing tool is added, you can make changes to suit the specific AI agent’s needs.

-   **[Now Assist AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/na-aia-reference.md)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the \[sn\_aia\_property\] agent system property.


-   **[Monitor more AI agent analytics in the AI Agent Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/ai-agent-dashboard.md)**

Two new pages have been added to the AI Agent Analytics dashboard, giving administrators more indicators, visualizations, and breakdowns to track AI agent performance and usage.

-   **[Exploring Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/exploring-ai-agents.md)**

Impersonation in Now Assist records transactions done by an AI agent in the name of the AI agent who executes the agentic workflow.


</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for App Engine

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Collaborative Work Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[More easily identify changes when previewing and updating applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/sns-app-gen-using-landing.md)**

When previewing an application, any requested changes made by the Now Assist for app generation skill are listed when the preview pane loads.

-   **[Edit applications without having to change the scope manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/sns-app-gen-review-apps.md)**

When editing applications, the Now Assist for app generation skill now changes the scope that you’re working in to the scope of the application automatically.

-   **[More easily query Analytics Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/analytics-assist-landing-page.md)**

Analytics Generation now uses a semantic filter instead of Natural Language Query \(NLQ\), resulting in less rigid requirements for queries.


-   **[Improved query engine for Analytics Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/analytics-assist-landing-page.md)**

Starting in Yokohama Patch 1, analytics generation supports GPT-4o for generating queries, to provide better accuracy in responses. These improvements include support for up to two levels of dot-walking based on user utterances.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **[Triage cases agentic workflows enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/case-resolving-use-case.md)**

Added new standalone AI agents to check duplicate cases and split some existing standalone AI agents to focus on more specific tasks. The AI agents available are the Triage cases planner AI agent, Context validator and analyzer agent, Duplicate identifier AI agent, Informational queries AI agent, Transactional queries AI agent, Case creation AI agent, Entity extraction AI agent, Document verification AI agent, and Email response AI agent.

-   **[Now Assist in Portal case form enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-ai-search-with-q-a-within-the-portal-form.md)**

Added the new **Ask Now Assist** button that opens a contextual chat window so that a requester can carry the conversation forward. If no results are found or if the requester isn’t satisfied with the result, they can get further assistance by selecting the button to chat and get an answer, which helps to avoid case creation.


Yokohama Early Availability

-   **[Email reply recommendations enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/generate-email-reply-recommendations.md)**

Refined the AI-generated reply recommendation to create the best response for users by applying tone changes in the Now Assist context menu. Additional tone options, including casual, formal, and sympathetic, are available.

-   **[Chat reply recommendation enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.md)**

Added the chat reply recommendation enhancements to respond in a conversational tone and get feature parity in the Now Assist Admin console:

    -   Refined the AI-generated reply recommendation to create the best answer for your users by applying tone changes in the Now Assist context menu. Additional tone options, including casual, formal, and sympathetic, are available.
    -   Added parity with the chat summarization Now Assist Admin console capabilities. The Now Assist Admin console can specify the portal and channels for chat reply recommendations and assign additional support roles.
-   **[Case summarization enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-for-csm/summarize-a-call-by-using-now-assist-for-customer-service-management-csm.md)**

Detailed feedback option is now available for negative feedback \[Omitted image "thumbs-down-outline-24.svg"\] Alt text: thumbs down icon in the generated case summary.

Xanadu Patch 7: Extended the capabilities of the case summarization feature so it can now be used on custom tables.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Removed prompt headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-for-field-service-management-fsm/cust-now-assist-fsm-wot-summarization-skill.md)**

The prompt headers have been removed from the work order summarization skill to support third-party Large Language Models \(LLMs\). You can now customize prompts via a hyperlink to the Now Assist skill.


</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **Flow name**

The Resolve noncritical HR cases flow has been renamed to Resolve HR cases flow.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-agentic-aia.md)**

Four AIOps AI agents have been removed from the analyze alert impact agentic workflow as they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/using-now-assist-for-itsm.md)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization
-   **Yokohama Patch 6 [Removing the prompt headers from the Customize prompt screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-itsm-skill.md)**

The prompt headers have been removed from the Customize prompt screen in the Incident summarization and Change summarization skill to support third-party Large Language Models \(LLMs\).

-   **Yokohama Early Availability[System property to display knowledge article templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/Now-Assist-generate-article-SOW-itsm.md)**

Display Knowledge article templates that you can use to create articles by using a system property. In earlier releases, the templates were displayed by default.

-   **Yokohama Patch 3 [IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-catincidents-usecase.md)**

The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.

The following AI agents have been added to the workflow:

    -   Link major incident AI agent
    -   Link incident to problem AI agent
The Incident categorize AI agent has been renamed to Categorize incident AI agent.


</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


</td></tr><tr><td>

Now Assist for Order Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Security Incident Response

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The following Now Assist skills for Now Assist for Security Incident Response and Now Assist for Vulnerability Response are activated by default.

    -   Security incident summarization \(SIR\)
    -   Resolution notes generation \(SIR\)
    -   Post incident analysis \(SIR\)
    -   Security incident recommended actions \(SIR\)
    -   Correlation insights generation \(SIR\)
    -   Security incident quality assessment \(SIR\)
The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The following Now Assist skills for Now Assist for Vulnerability Response are activated by default.

    -   Recommend preferred solution for VIT \(VR\)
    -   Vulnerable item de-duplication \(VR\)
    -   Approval Recommendation \(VR\)\(USEM\)
    -   Security Exposure Management \(SEM\) Insights \(VR\)\(USEM\)
    -   SPC Setup Connector \(Security Posture Control\)
The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/auto-complete-suggestion-types-na-ais.md)**

Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/semantic-search-ais.md)**

Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.


-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md)**

If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.

-   **[Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md).

-   **[Now Assist Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-catalog-ordering-gr.md)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md).


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Automated obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-na-reminder-agentic-wf.md#section_tgm_mt3_dhc)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-na-review-obligations.md)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-conf-obligation-extraction.md)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-agentic-use-conv-search.md)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/now-llm-model-updates.md)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Extract metadata from signed contracts automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-na-reminder-agentic-wf.md)**

Use the AI agents in the Manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/metadata-extraction-use-case.md)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case available in the base system.


-   **[Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md)**

Create a use case and its associated fields for contract metadata extraction in the Now Assist Admin console to define the information that you want Now Assist to detect in a signed contract.

Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.

-   **[Configuring contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/contract-management-pro/cmpro-conf-contract-analysis.md)**

Create a use case and its associated question groups for contract analysis in the Now Assist Admin console to identify the non-standard and missing clauses in a contract.

Create a clause mapping Now Assist Admin console to map question groups of a use case to active clauses in the clause library to display suggestions for non-standard clauses in a contract.

Create an expected response mapping in the Now Assist Admin console to map questions of a use case to an expected response to identify the non-standard clause in a contract.

Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for contract analysis.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-and-visual-insights-ai-agent.md)**

Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-and-visual-insights-ai-agent.md)**

Generate a summary of document and image attachments with the document and visual insights AI agent.


</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[View recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/expl-view-recommended-actions.md)**

AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/qg-supported-query-operations.md)**

Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/querygen-segments.md)**

Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for indicator sources or modules on domain-separated instances.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Query Generation skills are active by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/enable-query-generation.md)**

If the Generative AI Controller plugin is activated, the skills for Query Generation are activated by default.

-   **[Greater visibility into the Query Generation process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/ask-expl-questions.md)**

When you call Query Generation from AI Data Explorer or another application, you see each state that the query and response goes through before completing.

-   **[Multi-table source support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/ask-expl-questions.md)**

Query Generation supports related table conditions and dot-walking in queries.

-   **[Get insights and visualizations for Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/workflow-data-fabric/create-integrations-applications.md)**

Ask AI Data Explorer information about Workflow Data Fabric data and get insightful responses. You must first add the Workflow Data Fabric tables to the Query Generation Semantic Table Configuration table.

-   **[Use database views in queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/add-table-semantic-layer.md)**

Generate visualizations or ask AI Data Explorer about data kept in database views, like SLA data. You have to add the database views to the Semantic Table Configuration table.


-   **[Add tables to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/add-table-semantic-layer.md)**

Choose which tables your users can query with generative AI for data analysis.

-   **[Monitor the health of the Query Generation back end](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/querygen-health-page.md)**

View the state of Now Assist for Platform Analytics LLM, plugins, system properties, components, and dependent products.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Conversational Platform Now Assist skills are active by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md)**

The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.md)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/now-assist-in-virtual-agent/web-search-requestor.md)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md)**

If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


-   **[Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-standard-chat.md)**

The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


-   **[Dynamic Translation calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/translation-for-now-assist.md)**

If native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.


</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Email redirection behavior for links in major on-call schedule email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/on-call-scheduling/create-update-schedule-oncall.md)**

In all major on-call schedule or shift email notifications, you can now decide where the links to an on-call schedule or shift record are redirected. Instead of an on-call schedule or shift record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call schedule or shift record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
    -   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[Result types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/operational-sustainability-management/create-manual-metric-definition.md)**

If you have the ESG manager \[sn\_esg.metric\_manager\] role, you can now configure either text, choice, or HTML format options for responses to qualitative metric data tasks that are related to manual metric definitions, including both initial and overridden responses. These options help you achieve more precision and detail in your data collection process.

-   **[Metric data table filters and side panel enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/operational-sustainability-management/metric-data-table.md)**

If you have the ESG data owner \[sn\_esg.data\_owner\] role, you can now apply filters by using the filter menu and reject or approve tasks from the metric data table side panel. Data owners can now multi-submit and assign approvers to multi-approve or reject tasks, with the option to use choice and HTML response formats.

-   **[Data owner assignment types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/operational-sustainability-management/create-manual-metric-definition.md)**

If you have the ESG Manager \[sn\_esg.metric\_manager\] role, you can now configure the Data Owner Assignment type to be either simple or advanced for manual metric definitions. When you select the Simple option, the system assigns the specified Data Owner or Data Owner Group to the Metric Data Task. If you choose the Advanced assignment option, which is available with the GRC: Approver Configurator application, you can set custom configuration conditions, tables, or data owners to dynamically assign data owners.

-   **Table added to the GRC: Metrics application**

The following tables were added to the GRC: Metrics application:

    -   sn\_grc\_metric\_import\_job
    -   sn\_grc\_metric\_data\_import
    -   sn\_grc\_metric\_st\_import\_log
    -   sn\_grc\_metric\_st\_transform\_history
    -   sn\_grc\_metric\_import\_template
-   **Table added to the ESG content accelerator application**

The sn\_esg\_content\_issb\_citation table was added to the ESG content accelerator application.

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

Operational Technology \(OT\) Manager Foundation

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md)**

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[OT device related items and related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/ot-assets-related-links-and-lists.md)**

The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\], and Firmware Install \[cmdb\_firmware\_install\] related lists were added to the OT view on IT and OT classes to view the following information:

    -   Information related to the OT device populated through the integrations and captured as Key Value pairs.
    -   Software installed on the OT device if Software Asset Management isn't available.
    -   Firmware associated with the OT device.
You can view these related lists on the ServiceNow AI Platform® and in the Industrial Workspace Admin.

-   **[OT Excel SGC - Import Task list module in the Industrial Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/create-import-task-excel-sgc.md)**

The OT Excel SGC - Import Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the import task functionality for the Service Graph Connector for Microsoft Excel.

-   **[OT Excel SGC - Remediation Task list module in the Industrial Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/create-remediation-task-for-validation-errors.md)**

The OT Excel SGC - Remediation Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the remediation task records created from an import task.

-   **[View and edit device to device connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/view-device-to-device-connections.md)**

The Device to Device Connections list has been added to the OT Network menu available in the Industrial Workspace List view. You can view the device connections in detail using this list. Also, the Device to Device Connections related list was added to the **Related Records** tab on the OT device record in the ServiceNow AI Platform.

-   **[Is Virtual field for OT devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/ot-assets-form.md)**

Identify whether an OT device is virtual through the **Is Virtual** field added to the OT device form in the Industrial Workspace.

-   **[OT Subnet Mappings related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/ot-assets-related-links-and-lists.md)**

The OT Subnets related list has been renamed OT Subnet Mappings in both the Industrial Workspace and the ServiceNow AI Platform when viewing an OT device record.

-   **[__Manufacturer__ and __Model Number__ fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/ot-assets-form.md)**

The **Manufacturer** and **Model Number** fields have been removed from the OT device list and form views on both the ServiceNow AI Platform® and in the Industrial Workspace.

-   **[OT Devices tab data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/industrial-workspace/ot-manager-dashboard.md)**

The following data available in the **OT Devices** tab of the OT Manager dashboard has been moved to the Operational Technology Visibility dashboard.

    -   New OT devices discovered
    -   Inactive OT devices
    -   OT Devices overview
        -   Total CMDB OT devices
        -   Unclassed OT devices
        -   Unassigned OT devices
        -   Unmapped OT devices
    -   OT devices by category
        -   Supervisory systems
        -   Control systems
        -   Field devices
        -   Computers and servers
        -   Network Gear
        -   Industrial IoT
    -   OT devices by Purdue level
    -   OT devices by type \(Top Level\)
    -   OT devices by manufacturer \(Top Level\)
    -   OT devices by criticality

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   **[OT Vulnerabilities tab data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/industrial-workspace/operational-technology-vulnerability-response-dashboard.md)**

The following data that was available in the **OT Vulnerabilities** tab of the OT Manager dashboard has been moved to the OTVR \(PA\) dashboard:

    -   Total OT Vulnerable Items
    -   New OT Vulnerable Items
    -   OT Unassigned Vulnerable Items
    -   OT Vulnerable Items by State
    -   OT Vulnerable Items by Risk Rating

</td></tr><tr><td>

Opportunity Marketplace

</td><td>

-   **[Import Project Workspace project information to create an opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/opportunity-marketplace/egd-create-other-opportunities.md)**

Opportunity Marketplace opportunity owners can create Project Opportunity types by importing projects from the ServiceNow® Project Workspace.

**Note:** Creating a project opportunity type by importing a project file is only available to users with both ServiceNow Project Workspace and Opportunity Marketplace installed.

An opportunity owner must have the following roles assigned to them to create a Project type opportunity by importing project details from Project Workspace.

    -   **reource\_user [Resource management process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/resource-management/r_ResourceManagementProcess.md)**

If you’re assigned the resource\_user role, you can be a resource requester.

    -   **[sn\_ppm\_read](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/ppm-collaboration/business-stakeholder-role-ppm.md)**

The sn\_ppm\_read role provides read-only access to the Portfolio, Program, and Timecard dashboards along with the Resources report to the assigned users.

-   **[Select multiple user criteria groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/opportunity-marketplace/egd-create-other-opportunities.md)**

Opportunity owners can select multiple user criteria groups from the **Who can views this opportunity?** field on the Opportunity details page. For more information, see [Create opportunities in Opportunity Marketplace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/opportunity-marketplace/egd-create-other-opportunities.md).


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Migrate more features to Platform Analytics from the Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/data-migration.md)**

Migration scripts are improved to support more features. All migration script improvements are applied automatically on upgrade to content that was previously migrated in compatibility mode.

    -   Data table configurations are migrated from the Core UI to Platform Analytics data visualizations.
    -   Dashboard groups are migrated to dashboard categories.
    -   Pareto charts are migrated.
    -   List component border changes are migrated.
    -   Follow/unfollow filter settings are migrated for Lists.
-   **[Use more Core UI features in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/data-mig-unmigrated-content.md)**

Several data visualizations have been enhanced to match the capacities in Core UI reports and widgets. The migration script supports these enhancements. Each of these enhancements has an entry in the release notes with links to the product documentation.

    -   Use the new Box plot data visualization.
    -   Configure **Follow filters** per metric on bar or time series visualizations with multiple metrics.
    -   Sort values by name, report range, and element order on time series visualizations of table data.
    -   Choose an aggregate or separate view of breakdown elements on time series visualizations of indicator data.
    -   Select dates from business calendars on time series visualizations.
-   **[Trend by Business calendars in time series data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/config-dv-time-series-table-data.md)**

Business calendars are a **Trend by** option for table data sources on time series visualizations. \(Core UI feature gap\)

-   **[Use a Fiscal calendar in date filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/create-date-filter-workspace.md)**

If your instance has Fiscal calendars installed, you can choose relative data ranges from that calendar.

-   **Export [dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/export-pae-dashboard-ppt.md) and [data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/export-visualization-vd.md) to PDF and PPT**

Export dashboards and data visualizations to PDF or Microsoft PowerPoint files at will or in [scheduled emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/schedule-export-dboards-data-viz.md).

-   **[Show breakdown elements separately on time series visualizations of indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/config-dv-time-series-ind-data.md)**

Show multiple elements in the chart separately rather than as an aggregate value by turning on the **Show filter as separate series** option. \(Core UI feature gap\)

-   **[Lock editing on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/edit-db-in-ac.md)**

Ensure that only one person can have a dashboard open for editing at one time through the edit lock on dashboards. If you are locked out of editing a dashboard, you see who the current editor is.

-   **[Access indicator record or scoresheet from KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/access-indicator-record-scoresheet.md)**

Navigate either to the record of the indicator you are exploring or its scoresheet through KPI Details. Appropriate roles are required.

-   **[Export records that underlie an indicator from KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/show-compare-edit-records.md)**

With **Show records** activated in KPI Details, you can export the list of records in one of several formats, either as a local download or as an email attachment.

-   **[Hide axes for bar visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/create-dv-bar-ac.md)**

Control the display of axes on bar charts. On horizontal bar charts, you can hide the y-axis. On vertical bar charts, you can hide the x-axis.

-   **[Cache indicator scorecard data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/data-caching-pa.md)**

Indicator scorecards now support data caching.

-   **[Group by elements more efficiently in data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/select-group-runtime.md)**

Specify the maximum number of elements in a Group By you want to retrieve through the **Max number of groups** option. Previously, all elements from the database were retrieved and then sorted.

-   **[Prefetch dashboard layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/configure-dashboard-data-broker.md)**

If you have a dashboard component on a page in your own workspace, improve performance by using a preset to configure a data broker that pre-fetches static JavaScript, such as layout.

-   **[Call multiple visualizations together](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/local-data-instance-multi-viz.md)**

For a technical dashboard, if you have multiple data visualizations of the same type calling the same data source, configure a data resource to make a single call for all of them.

-   **[Improvements to time-series visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/config-dv-time-series-table-data.md)**
    -   Simplify identifying specific values on line, spline, area, or step charts through the **Show markers** option, which displays a symbol at each data point.
    -   Sort by name, report range, group bucket, and element order. \(Core UI feature gap\)
-   **[Improvements for visualizations that show multiple metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/chart-options-multi-metrics.md)**
    -   In time series visualizations, provide viewers an alternative group by, where the viewer chooses the group-by value at runtime, for up to 3 data sources. \(Core UI feature gap\)
    -   Set whether individual metrics follow filter components on the page or dashboard in both bar and time series visualizations. \(Core UI feature gap\)

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **Change triggers in any playbook**

Edit triggers when you duplicate a playbook, in a variant, etc.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Tagging of information object tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/tag-io-with-pi.md)**

Use the **Data classification** field to tag information objects instead of using the tag icon.

-   **[Initiating privacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/privacy-workspace/send-privacy-asmt-from-pa.md)**

When you initiate a privacy assessment from either an entity or a processing activity, you’re no longer redirected to the **Create new privacy assessment form**, instead, a new pop-up window appears where you can specify all the assessment details.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Multiple configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/sales-and-order-management/multiple-child-offering-configurations.md)**

Define child product offerings that can have multiple configurations in configurable opportunities, quotes, and orders. Agents can clone or split a child product offering to create multiple product offering instances. Each quantity for an offering instance can then have its own unique configuration.

-   **[Transient product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/sales-and-order-management/configuring-transient-products.md)**

Define single-use product offerings, such as installation services or consulting services, as transient products that are fulfilled in ServiceNow Order Management. After orders for transient products are fulfilled, sold product or product inventory records are created but have an Inactive status. Move, Add, Change, Delete \(MACD\) actions aren't supported for the sold product or product inventory records of transient products.


-   **[Configurable pricing plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/sales-and-order-management/configuring-pricing-plan.md)**
    -   Apply Renewal Adjustment step: This new step determines whether a contract renewal adjustment, either a markup or markdown amount or percentage, is to be calculated and applied. For example, as a pricing admin, you might want to apply a pricing uplift of a fixed amount at contract renewal. This renewal adjustment step is enabled by default, but you can change or remove it in a custom configurable pricing plan.
    -   Extension point updates: The ListPriceExtensionPoint, which gathers the data needed to make required adjustments, now includes the adjustment data for contract renewals.
-   **[Volume-based pricing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/sales-and-order-management/configure-volume-pricing.md)**

Set volume discounts for product offerings based on the product quantity.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Heatmap enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/project-workspace/use-resource-mgmt-prj-wksp.md)**

The resource allocation heatmap displays the resource status, capacity, and utilization, enabling efficient planning and allocation based on availability and workload.


</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Constituent Service Dashboard Migration to Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/public-sector-digital-services/constituent-services-dashboard.md)**

The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when the user loads or upgrades to the Yokohama release. The dashboard migration to Next Experience enables you to visualize historical and real-time process statistics in role-based dashboards, which enable individual stakeholders to make informed decisions. The new dashboard can be accessed by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[Changed fields for the Unattended Robot application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/rpa-hub/set-up-rpa-runtime.md)**

In the Unattended Robot dialog box, the **RPA Hub** field name has been changed to **Instance URL**.

-   **[Embedded Task Automation in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/rpa-hub/embedded-task-auto-rpa.md)**

Trigger attended bot processes \(attended automations\) from the ServiceNow forms in the Workspace experience apart from initiating them from a classic UI or the Attended Robot application.

-   **[Microsoft Software Installer \(MSI\) compatibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/rpa-hub/download-installer-rpa.md)**

Older MSIs that are related to Attended Robot and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(12.0.X\) of RPA Hub. For Unattended Robot, the latest MSI must be installed, as it is not backward compatible.

However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the SSH connector in version 12.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
If robot machines use older MSIs than the current instance version, they won't have the new features from later versions. For example, features released after version 10.0 won't work in version 10.0 MSIs. Only features from version 10.0 are available in that version.

-   **[TerminateByName component behavior change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/rpa-hub/use-sysprocess-terminatename.md)**

The TerminateByName component stops processes or applications only within the current user session.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Overview page of regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/regulatory-change-management-service-portal/list-view-of-reg-alerts.md)**

The Overview page for regulatory alerts includes a drop-down menu that enables you to track the progress of a regulatory assessment. Additionally, you can view the counts of completed, open, and overdue regulatory assessments.

-   **[Home page updates for Regulatory Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/regulatory-change-management-service-portal/rcm-workspace-for-managers.md)**

On the Regulatory Change Management home page, within the Tracking section, a new drop-down menu has the Regulatory Assessments or Risk Assessments options. With these options, regulatory change managers can see the number of open and overdue assessments to help them efficiently monitor the status of their assessments.

-   **[Regulatory assessments in the Tasks pane](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/regulatory-change-management-service-portal/regulatory-assessment-in-rcm.md)**

The Tasks pane in the Compliance Workspace now displays all the Regulatory assessments.


-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Request Management

</td><td>

-   **[Sorting configuration items in requested item forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/request-management/create-request-workspace.md)**

The list of configuration items \(CIs\) displayed for the **Configuration item** field in the Requested item form is now displayed and sorted based on the CI names in alphabetical order instead of sorting by CI class and then presenting the CI names in alphabetical order within a class. This change means you can determine whether a particular CI is available more quickly.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[New resource heatmap view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/resource-management/using-rmw.md#section_fmx_yrl_b1c)**

The resource allocation heatmap view provides more relevant information such as resource status, remaining capacity, and utilization of resources which helps resource managers to plan efficiently and allocate the resources based on their availability, bandwidth, and work requirements.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/security-operations-landing-page.md)**

<table id="table_h5p_xyl_sdc"><thead><tr><th>

Integration name

</th><th>

Integration changes

</th></tr></thead><tbody><tr><td>

Microsoft Teams Chat

</td><td>

Simplified the setup of Microsoft Teams Chat integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/integrate-msim-sharepoint.md).

</td></tr><tr><td>

Microsoft SharePoint

</td><td>

Simplified the setup of Microsoft SharePoint integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/integrate-teams-msim.md).

</td></tr><tr><td>

Security Incident Response Integrations

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Get Log Data Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/get-threat-log-data.md)
-   [Get WildFire Data Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/enrich-wildfire-data.md)
-   [Get started with the Microsoft Exchange On-Premises integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/activate-configure-ms-exch-on-prem-integ.md)
-   [Microsoft Exchange - Perform Email Search and Deletion flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/ms-exch-perform-email-search-deletion-wf.md)
-   [Get AutoFocus Session Info Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/search-for-malicious-content.md)


</td></tr><tr><td>

Security Incident Response Orchestration

</td><td>

Workflow was migrated to Workflow Studio in the section [Run procdump flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/invoke_procdump.md).

</td></tr><tr><td>

Security Operations common functionality

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/integration-capabilities.md)
-   [Security Operations Integration- Block Request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/block-request-capability.md)
-   [Security Operations Integration- Email Search and Delete capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/email-search-capability.md)
-   [Security Operations Integration- Enrich CI capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/enrich-ci-capability.md)
-   [Security Operations Integration- Enrich Observable capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/enrich-observable-capability.md)
-   [Security Operations Integration- Get Network Statistics capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/get-network-statistics-capability.md)
-   [Security Operations Integration- Get Running Processes capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/get-running-processes-capability.md)
-   [Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/isolate-host-capability.md)
-   [Security Operations Integration- Publish to Watchlist capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/pubish-to-watchlist-capability.md)
-   [Security Operations Integration- Sightings Search capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/sightings-search-capability.md)
-   [Security Operations Integration - Threat Lookup capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/sec-ops-threat-lookups-capability.md)
-   [Change the order of flow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations/change-wf-execution-order.md)


</td></tr></tbody>
</table>-   **[Other additional Security Incident Response setup tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-incident-response/t_ConfigureSIM.md)**

View security incidents with read access and update security incidents with write access without any defined security role.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Using the email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-email-interaction-page.md)**

Manage and view customer-related information and past conversations while interacting with customers via email.

-   **[Using the Now Assist in Virtual Agent enhanced chat in self-service portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/nass-portal.md)**

Receive comprehensive and detailed answers with intelligent search and conversational experiences using Now Assist in Virtual Agent. The search results are synthesized from Knowledge Base articles, Virtual Agent articles, and catalog items with links to the sources. The agent retains conversation context across multi-turn questions, promoting continuity and relevance in responses.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Incident record page changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/view-inc-record-info-contextual-sidepanel.md)**

The Incident record page has the following changes:

    -   The caller card is placed first on the Record information side panel for tier 1 agents.
    -   The origin card itself is no longer clickable to reduce usability issues with the card and its clickable elements.
-   **[Reference field behavior changes in SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/view-update-inc-overview-tab.md)**

Selecting any reference field in SOW now displays only the recent selection values instead of automatic searching and displaying the results of the field values available in the system. This change increases the overall performance of the reference fields. By default, this change is enabled. To revert this change, set the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property to set to `true`.

-   **[Viewing Assign to me option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/users-sow-itsm.md)**

Users with the incident\_read role can no longer view the **Assign to me** option for an incident record.

-   **Email component issues on SOW Incident**

Email components are now accurately displayed for SOW Incident when the email is selected from the activity stream, stacked view, or email template is applied.

-   **Resetting filter conditions**

Filter conditions are now reset when switched from one related list to another related list.

-   **Saving interaction record loads recent tasks**

When a new interaction record is created and saved, the sidebar now loads record Information instead of recent Tasks.

-   **[Problem Management state transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/problem-management/understanding-state-mgmt-transitions.md)**

Sections that are configured to be expanded now automatically expand when you transition to a new state, without requiring a page reload.

-   **[GenAI email templates for communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/compose-communication-mim-sow.md)**

Use the GenAI capabilities for composing email with GenAI email templates in all major incident communications. The GenAI email templates are visible in a separate section when the email templates field is selected and the following conditions are met:

    -   Any GenAI variable is available in the email templates.
    -   Now Assist for ITSM is installed and activated.
    -   GenAI skills are enabled.
    -   User have the required roles to execute the GenAI skills.
-   **[Close resolved incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/close-resolved-incident-sow.md)**

Close an incident in **Resolved** state using the itil\_admin user role.

-   **[Resize modals on the SRP and list pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-operations-workspace/srp-service-operations-workspace.md)**

Ensure flexibility and efficiency by enabling users to resize the modals on the SOW SRP and list pages. This helps in adjusting screen space allocation, enabling multi-tasking, and optimizing content visibility for different tasks and screen sizes. 


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Use ECMAScript 2021 \(ES12\) JavaScript mode in server scripts for widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/service-portal/widget-dev-guide.md)**

Use features supported in the ECMAScript 2021 \(ES12\) JavaScript mode in server-side scripts for widgets by selecting **Turn on ECMAScript 2021 \(ES12\) mode** from the widget record or Widget Editor. For information about features supported in the ECMAScript 2021 \(ES12\) JavaScript mode, see [JavaScript engine feature support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/javascript-engine-feature-support.md).

-   **[Define roles for page route maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/service-portal/reroute-page.md)**

Control which users are redirected to a new page based on a page route map. Specify the user roles to apply in the Page Route Map form.

-   **[Improved redirection for single sign-on \(SSO\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/service-portal/c_SPSSOLoginAndRedirects.md)**

Improved the experience of logging in to portals that use single sign-on \(SSO\) authentication by redirecting to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

-   **[Enforce providing comments when rejecting requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/service-portal/approvals-widget.md)**

Require approvers to provide comments when rejecting a request from the Approvals widget. Administrators can enable requiring comments from the widget instance options.

-   **[Check cross-scope privileges to a table with the Form widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/service-portal/form-widget.md)**

Validate access to tables from which the Form widget fetches data. The Form widget checks for the necessary cross-scope privileges to a table by default.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[Updated Access Control Lists \(ACLs\) for Transaction tables and Session Management tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-control/exploring-access-control-list.md)**

The ACLs for a number of Transaction Management tables and Session Management tables have been updated to enhance security using a combination of Deny and Allow ACLs. All new ACLs have a security attribute. You must have the security attribute to add to the role list of an ACL. For more information, see [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-control/t_CreateAnACLRule.md), [Deny-Unless ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-control/acl-denial-behavior.md), and .

The updated Transaction Management tables include:

    -   syslog
    -   syslog\_ajax
    -   syslog\_email
    -   syslog\_transaction
    -   syslog\_script
The updated Session Management tables include:

    -   sys\_audit
    -   sys\_security\_acl
    -   sys\_user\_auth
    -   sys\_user\_session
-   **[Configuring plugins for the TinyMCE HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/configuring-the.md-plugins-for-tinymce.md)**

The Accessibility Checker \(a11ychecker\) plugin is now available in the TinyMCE HTML editor. The plugin identifies WCAG and Section 508 accessibility violations and provides an auto-repair feature where applicable. To configure the plugin, see [Change the TinyMCE HTML editor plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/configuring-the.md-plugins-for-tinymce.md). Additional configurations to the accessibility rules, like changing the WCAG level and HTML versions can also be done via **TinyMCEconfigscript** script.

-   **[Field types supported in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/r_FieldTypes.md)**

The following field types are now supported for use in a configurable workspace:

    -   Documentation\_field
    -   Domain\_path
    -   HTML\_Script
    -   Long
    -   Longint
    -   multi\_small
    -   Order index
    -   Radio
For more information, see [Field types reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/r_FieldTypes.md).

-   **[Specify the tables that a REST API access policy restricts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/authentication/create-api-access-policy.md)**

Specify the tables that a Table REST API access policy applies to on the API Access Policy form.

-   **[Use ISO currency codes with the FX Currency field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/currency-administration/fx-currency.md)**

Use three-digit ISO 4217 currency codes from the **Numeric code** field on the Currency \[fx\_currency\] table with fields of the FX Currency field type.

-   **[Sorting according to the session language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/system-localization/sorting-session-language.md)**

Configure whether string values in columns are sorted according to the user's session language or English.

-   **[Columnstore index type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/table-administration-and-data-management/t_CreateCustomIndex.md)**

Optimize data storage and retrieval by creating a columnstore index. This index type is available with RaptorDB Professional.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Subcommands replaced with parameters on the auth command](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/servicenow-sdk-cli-commands.md)**

Configure authentication credentials with the `--add`, `--delete`, `--list`, and `--use` parameters of the `now-sdk auth` command.

-   **[Dependencies command installs type definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/servicenow-sdk-cli-commands.md)**

Download TypeScript type definitions for Glide APIs and script includes from a ServiceNow instance based on the scripts in your application.

-   **[Build command includes --frozenKeys parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/servicenow-sdk-cli-commands.md)**

Validate that the auto-generated `keys.ts` file is up to date for continuous integration \(CI\) builds by setting the `--frozenKeys` parameter to true with the `now-sdk build` command.

-   **[Deploy command renamed install](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/servicenow-sdk-cli-commands.md)**

Install or update an application on a ServiceNow instance using the `now-sdk install` command.

-   **[Automated Test Framework Test API supports two-way synchronization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/atf-test-now-ts.md)**

Synchronize changes to Automated Test Framework tests made outside of source code into source code definitions and back to metadata.

-   **[Table API supports licensing configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/table-api-now-ts.md)**

Create a licensing configuration \[ua\_table\_licensing\_config\] to track subscription counts for a table with the licensing\_config object in the Table API.

-   **[Table API supports remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-sdk/table-api-now-ts.md)**

Create a remote table with the scriptable\_table property in a Table object.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Modify an app's settings in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/modify-an-apps-settings-in-servicenow-studio.md)**

The App settings icon in ServiceNow Studio used to open a small modal where only a few settings could be updated and the app could be deleted. In this release, the icon opens a Core UI view of all the app settings and related links for the app.

-   **[Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md)**

As of version 27.2.4, the available options at the success page for creating an application changed from **Go to app dashboard** to **View App Details** and **Create File**.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/auto-reflow.md)**

The Software Asset configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.

-   **[Publisher optimizations dashboard for Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/software-asset-management/pub-opt-microsoft.md)**

The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Changes in planning item forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/scenario-planning-in-spw/epic-form.md)**

The dates in the **Planned start date** and **Planned end date** fields are editable for all planning item types other than Demand and Project planning item types. Also, the **State** field is editable for EAP planning items and its child items.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Allocation charts reflect only active users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/subscription-details-v2.md)**

The Allocation summary and Allocation history charts on the subscription details page reflect only the subscriptions allocated to active users for each month following the upgrade.

-   **[Auditing App Engine V1 usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/allocating-custom-tables-subscr-apps-v2.md)**

The App Engine Usage dashboard has been restored. For details on auditing App Engine V1 usage, see the [Auditing App Engine v1 \[KB0999383\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999383) article in the Now Support Knowledge Base.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

Now Assist usage measurement is evolving. If your instances are below Yokohama Patch 12, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement types. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Hidden user-based subscription allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/subscriptions-overview-v2.md)**

To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


</td></tr><tr><td>

System Update Sets

</td><td>

-   **Application installations**

You can add specific applications or versions as an app installation and configure to track them in an update set.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Pre-populate responses using questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md)**

If you have the Third-party risk assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or Third-party risk manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can enable third-party and engagement contacts to review and update responses only if necessary by pre-populating questionnaires for engagements and entities with responses from completed questionnaires that are associated with the same third party. The attachment, duration, and signature type responses are excluded. This feature also helps ensure data consistency and accuracy.

-   **[Microsoft Excel questionnaire template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/tprm-excel-template-support.md)**

Streamline the due diligence process by enabling third-party and engagement contacts to respond to questionnaires using a Microsoft Excel template by downloading the questionnaire as a template, completing it according to the included instructions, and importing the final version into the Third-party portal. This feature update enhances flexibility by enabling third-party and engagement contacts to provide information outside the third-party portal. Third-party risk assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and Third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access this feature and respond to questionnaires on behalf of Third-party and engagement contacts through the Vendor Management Workspace.

-   **[Codes and additional identification information for ICT third-party service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-ICT-thirdparty-serv-prov-form.md)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by adding additional code types and a legal name to third-party and third-party engagement records in the digital resilience third-party registers within the Vendor Management Workspace. Include this information when the legal name of a third party differs from its commonly recognized name, or when you need to record multiple identification codes like a EUID, LEI, or Country code. When supply chain, assessment, or contract records are associated with a third party or third-party engagement using the EUID code type, all relevant fields will be automatically populated.

-   **[Function types for ICT third-party service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-new-function-form.md)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], help ensure compliance with DORA regulations by using Business capability as an additional function type for function records in the digital resilience third-party registers within the Vendor Management Workspace.

-   **[Multiple legal entities making use of the services for contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-contract.md)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], add multiple legal entities that are using services as part of a contract record in the digital resilience third-party registers within the Vendor Management Workspace. Including all entities that are using services associated with a contract is essential for maintaining transparency, helping ensure compliance, and enhancing operational resilience.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Courses of Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/threat-intelligence-security-center/course-of-action.md)**

Renamed Course of Actions to Courses of Action.

-   **[Create Inbound Data Exclusion Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/threat-intelligence-security-center/define-filtering-rules.md)**

Renamed Inbound Filtering Rules to Inbound Data Exclusion Rules.


</td></tr><tr><td>

Upgrade Center

</td><td>

-   **[Upgrade Plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/upgrade-center/uc-upgrade-plan.md)**

Experience a seamless upgrade on your instance with the Upgrade Plan, offering the option to either include or bypass skipped records and customizations during its building.


</td></tr><tr><td>

Usage Insights

</td><td>

-   **New custom user property configuration**

An easy way to configure which user-related fields are available to use as filters and in user details. Configured user properties are available for all applications. Previously created custom user properties are no longer supported and must be recreated in the new UI.

-   **Country consent policies are set by default to No Consent Required**

Default country consent policies are now set to No Consent Required. If you have previously updated your country consent policies, they will retain the custom setting. Existing users who have set their tracking preferences will retain their settings. New users will not require consent for tracking unless you update your country consent policies.

-   **Longer user history**

Detailed data for users and sessions extended to two years.

-   **Optimized the way metrics are calculated**

Percent time on app and Average duration per page calculations changed compared to the application view in Xanadu or prior releases. Percentage time on app was **Percentage time on site** in Xanadu or prior releases.

-   **Client page load and Full page load aggregated in the same visualization**

All performance metrics associated with Client, Network, Page Load, and Server time are aggregated together.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[Test assistant options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/virtual-agent/test-llm-topics.md)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


-   **[Dynamic Translation calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/translation-for-now-assist.md)**

For Now Assist, if native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.

-   **[Table bot response control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/virtual-agent/table-bot-response.md)**

Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/integration-hub/visa-spoke.md#section_gsl_nw5_vyb)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Details Response Parser
    -   Submit Dispute Questionnaire
-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/integration-hub/visa-spoke.md#section_gsl_nw5_vyb)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.2 revision changes:

    -   Submit Dispute Questionnaire
    -   Hypersearch Request Builder
    -   Hypersearch Response Parser
    -   Create Dispute Pre-Arbitration Request Builder
    -   Create Dispute Pre-Arbitration Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Response Details Request Builder
    -   Look up Dispute Pre-Arbitration Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Details Request Builder
    -   Look up Dispute Pre-Arbitration Details Response Parser
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **[Updates made for Claroty CTD v5.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-vulnerability-response/connect-to-claroty-ctd-vr-integration.md)**

The following updates were made to support Claroty CTD v5.1:

    -   There's no limit now on the number of Common Vulnerabilities and Exposures \(CVEs\) that you can import.
    -   The **Minimum CVSS Score** field was replaced with the **CVSS V3 Score** field.

</td></tr><tr><td>

Workspace

</td><td>

-   **[Context-based suggestions with @mentions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/set-up-at-mentions.md)**

Receive suggestions for users with access to the record when using @ mentions.

-   **[Expand all tiles in the Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/activity-stream-expand-tiles.md)**

Set a user preference to keep all tiles in the Activity stream expanded across cases and user sessions.

-   **Access control security model for the Activity stream**

Data filters and access rules provide role-based access control for viewing and editing tables in the Activity stream.

-   **[Multiple records added from the multi-record associator load in the background](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/set-up-asynchronous-record-addition.md)**

Work on a record while the multiple records that were selected from the multi-record associator are added in the background.

-   **Attach display text to knowledge base links in the email composer**

Manage your email's appearance by attaching display text to knowledge base links.

-   **Infinite scroll for lists**

Use the Record List bundle to scroll through lists infinitely without pagination.

-   **Live updates for lists**

Use the Record List bundle to view live updates on lists without refreshing the page.

-   **Temporary lists available in the list menu**

Temporarily access personalized lists that are sent to you as links within the My Lists menu.

-   **Filter for hierarchy in condition builder**

The **is within hierarchy** field in the condition builder enables you to filter your list within a hierarchy instead of only direct reports.

-   **[AI filter assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/use-ai-filter-assist.md)**

Convert everyday language into an encoded query with AI filter assist.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **[View Zero Copy Connector for ERP software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-framework/view-erp-system-information.md)**

From the Zero Copy Connector for ERP system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-framework/erp-canvas-preview-entity.md)**

In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/release-notes-summaries.md)

