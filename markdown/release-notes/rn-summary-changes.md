---
title: Changes to Zurich features and products
description: Cumulative release notes summary on changes to Zurich features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/rn-summary-changes.html
release: zurich
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 164
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Changes to Zurich features and products

Cumulative release notes summary on changes to Zurich features and products.

Existing  products were updated and changed in Zurich. This includes the renaming of certain buttons or features.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   The Autonomous vs. supervised AI tools chart has been removed.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes in Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)**
    -   The AI asset inventory plugin structure has been updated.
    -   Product owner view: Added a role called AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\], which enables the Product Owner view experience with a personalized home page and enhanced visibility into AI assets to simplify task management.
    -   AI discovery: The Innovation lab store application \(AWS AI discovery plugin\) is decommissioned. Uninstall the AWS AI discovery plugin prior to installing the AI discovery plugin \(sn\_ai\_disc\).
    -   AI cases management has moved under the **AI cases** tab on the AI Control Tower home page.

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[AI risk and compliance home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/ai-risk-and-compliance-workspace.md)**

The **Risk and compliance** tab now features dedicated Risk overview and Compliance overview sections that enable you to continuously monitor the risk and compliance posture of your AI assets.

The Risk overview section is a filtered view of your AI assets that are based on inherent and residual risk levels so that you can make informed risk evaluations. The Compliance overview section displays the regulatory risk classification of AI systems, models, and datasets through donut charts. Additionally, you can see the compliance status of your AI assets in relation to applicable authority documents and internal policies.

-   **[Worknotes and comments in AI system records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/ai-system-airc.md)**

The AI system record now supports worknotes and comments. You can now document decisions, share updates, and provide context throughout the AI risk and compliance life-cycle. Worknotes and comments help improve the communication among stakeholders and ensure a comprehensive audit trail.

-   **Feature-specific administrator role enhancements**

Starting with version 21.1.1, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-suggestions-overview.md)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-preview-ui-new.md)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


-   **[Consumer-grade search experience for search portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/viewing-search-results-ais.md)**

The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/using-ais-next-experience-app.md)**

The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-facet-ais.md)**

Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **Improved display for grouped attachment search results**

When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


</td></tr><tr><td>

API

</td><td>

<table id="table_x1g_1mc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideSysAttachment - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideSysAttachmentScopedAPI.md)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngine - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/IdentificationEngineScopedAPI.md)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[ProducerV2 - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/ProducerV2ScopedAPI.md)

</td><td>

send\(\) - Added a return value and error handling.

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_RESTMessageV2API.md)

</td><td>

setHttpMethod\(\) - Added support for HEAD method calls via the **method** parameter.

</td></tr></tbody>
</table><table id="table_bq3_xc4_ghc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

1.7.1

</td><td>

2026-02

</td><td>

[LeadtoCashCore - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/LeadToCashCoreAPI.md)

</td><td>

createInstance\(\) now supports the **allowedContextTypes** parameter, enabling partial synchronization of updates or deletions for selected Related Parties back to the originating Opportunity. Previously, partial synchronization behavior was limited to quote line items only.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

1.6

</td><td>

2025-12

</td><td>

[LeadtoCashCore - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/LeadToCashCoreAPI.md)

</td><td>

To allow more complex business needs, getPrimitivesEPService\(\) supports the new **context.entityConfigId** parameter, which invokes createInstance\(\) script without any defined mapping using only the entity's configuration ID.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideAggregateAPI.md)

</td><td>

Remove support for groups in Dynamic Schema.-   addAggregate\(\)
-   addHaving\(\)
-   getDynamicAttributeValue\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

</td></tr><tr><td>

[GlideDynamicAttribute - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideDynamicAttributeAPI.md)

</td><td>

Remove support for groups in Dynamic Schema. -   getGroupName\(\)
-   getName\(\)
-   getPath\(\)
-   getType\(\)
-   isTransient\(\)

Remove getSysId\(\).

Remove GlideTransientDynamicAttribute API documentation because GlideDynamicAttribute and GlideTransientDynamicAttribute APIs provide the same solution.

</td></tr><tr><td>

[GlideRecord - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideRecordAPI.md)

</td><td>

Remove support for groups in Dynamic Schema.-   addQuery\(\)
-   getDisplayValue\(\)
-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   getValue\(\)orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setValue\(\)

</td></tr><tr><td>

[GlideSysAttachment - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideSysAttachmentGlobalAPI.md)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngineScriptableApi - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_IdentEngineScriptAPI.md)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_RESTMessageV2API.md)

</td><td>

setHttpMethod\(\) - Added support for HEAD method calls via the **method** parameter.

</td></tr></tbody>
</table><table id="table_nbf_qmc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Telecommunication Open APIs

</td><td>

3.1.0

</td><td>

2026-02

</td><td>

[Product Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)

</td><td>

When submitting a change payload with a new or updated service location \(via **productOrderItem.product.place.id**\), the request is now processed as a move order. This means that the product order remains the same but the service is fulfilled in the new designated location.-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)
-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2025-12

</td><td>

[Omnichannel Callback API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/omichannel-callback-api.md)

</td><td>

Added voicemail information to the callbackContext request parameter in the following endpoints:

-   POST api/sn\_omni\_callback/callback/create
-   POST api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

7.7.1

</td><td>

2025-12

</td><td>

[Trouble Ticket Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/trouble-ticket-open-api.md)

</td><td>

Now supports creating, retrieving, and filtering on the Service Problem Case ticket type.-   GET /sn\_ind\_tsm\_sdwan/ticket/troubleTicket 
-   GET /sn\_ind\_tsm\_sdwan/ticket/troubleTicket/\{id\}
-   PATCH /sn\_ind\_tsm\_sdwan/ticket/troubleTicket/\{id\}
-   POST /sn\_ind\_tsm\_sdwan/ticket/troubleTicket

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Product Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/product-catalog-open-api.md)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the product offering catalog.
-   **internalVersion**: Specifies the version of the product offering.
-   **prodSpecCharValueUse.​valueType**: Supports more complex product characteristic value types, like choice, check box, objects, and so on.
-   **version**: Specifies the external version of the product offering.

Enhanced the version and supports external system logic and complex characteristics.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/service-catalog-open-api.md)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the service specification.
-   **internalVersion**: Specifies the version of the service specification.
-   **specCharacteristic.valueType**: Supports more complex service characteristic value types, like choice, check box, objects, and so on.
-   **version**: Specifies the external version of the service specification.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Product Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the product order.
-   **internalVersion**: Specifies the version of the product specification.
-   **productOrderItem.product.productCharacteristic.valueType**: Supports more complex product characteristic value types, like choice, check box, objects, and so on.
-   **productOrderItem.product.productSpecification.version**: Specifies the external version of the product specification.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/service-order-open-api.md)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the service order.
-   **serviceOrderItem.service.serviceCharacteristic.valueType**: Supports more complex service characteristic value types, like choice, check box, objects, and so on.
-   **serviceOrderItem.service.serviceSpecification.internalVersion**: Specifies the version of the service specification.
-   **serviceOrderItem.service.serviceSpecification.version**: Specifies the external version of the service specification.

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tisc-api.md)

</td><td>

POST /sn\_sec\_tisc/threat\_intel\_data/observables now supports filtering observables on tags and taxonomies.

</td></tr><tr><td>

Accounts Payable Invoice Processing

</td><td>

v9.5.17

</td><td>

2025-08

</td><td>

[AP Invoice API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/ap-invoice-api.md)

</td><td>

The following endpoints now support attachments:-   POST sn\_spend\_intg/ap\_invoice/json
-   POST sn\_spend\_intg/ap\_invoice/xml

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Service Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/service-order-open-api.md)

</td><td>

The following endpoints now support complex service characteristic value types via the **serviceOrderItem.service.serviceCharacteristic.valueType** parameter:-   GET /sn\_tmf\_api/order/serviceOrder
-   GET /sn\_tmf\_api/order/serviceOrder/\{id\}
-   PATCH /sn\_tmf\_api/order/serviceOrder/\{id\}
-   POST /sn\_tmf\_api/order/serviceOrder

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Product Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/product-catalog-open-api.md)

</td><td>

The following productSpecification endpoints are updated to support complex product specification characteristic value types via the **productSpecCharacteristic.valueType** parameter:-   POST /sn\_tmf\_api/catalogmanagement/productSpecification
-   PATCH /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
-   GET /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
-   GET /sn\_tmf\_api/catalogmanagement/productSpecification

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/product-inventory-open-api.md)

</td><td>

The following endpoints now support complex product characteristic value types via the **productCharacteristic.valueType** parameter:-   GET /sn\_prd\_invt/product
-   GET /sn\_prd\_invt/product/\{id\}
-   GET /sn\_prd\_invt/productinventory
-   GET /sn\_prd\_invt/productinventory/\{inventoryId\}
-   POST /sn\_prd\_invt/product
-   POST /sn\_prd\_invt/productinventory

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Product Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf622_product_ordering-api.md)

</td><td>

The following endpoints now support complex product characteristic value types via the **productOrderItem.product.productCharacteristic.valueType** parameter:-   GET /sn\_ind\_tmt\_orm/order/productOrder
-   GET /sn\_ind\_tmt\_orm/order/productOrder/\{id\}
-   GET /sn\_ind\_tmt\_orm/productorder
-   GET /sn\_ind\_tmt\_orm/productorder/\{id\}
-   PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}
-   PATCH /sn\_ind\_tmt\_orm/productOrder/\{id\}
-   POST /sn\_ind\_tmt\_orm/order/productOrder
-   POST /sn\_ind\_tmt\_orm/productOrder

</td></tr><tr><td>

Virtual Agent API

</td><td>

4.0.0

</td><td>

2025-08

</td><td>

[Virtual Agent Bot Integration API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/bot-api.md)

</td><td>

New options for the **action** request body parameter with corresponding examples.POST /sn\_va\_as\_service/bot/integration

</td></tr></tbody>
</table>

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/work-with-invoice-exceptions.md)**

The Insufficient goods receipt exception has been enhanced to validate line-level quantities accurately when multiple invoices are submitted against a single purchase order even if a sufficient goods receipt exist.

The Insufficient Funds \(Line Amount\) functionality has been enhanced to perform validation of available funds at the invoice line level, matching each invoice line against its respective purchase order line when multiple invoices are generated for the same purchase order line.

The Insufficient Funds \(Header Amount\) logic has been enhanced to validate available funds at the invoice header level against the corresponding purchase order when multiple invoices are created for the same purchase order.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-search-analytics-dashboard.md)**

The performance metrics, trends, and charts for this dashboard have been refreshed to offer a cleaner visual experience.


-   **[AI Search analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-search-analytics-dashboard.md)**

The **Date range** interactive filter now enables you to access data from the last 180 days, rather than the last 90 days.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Thin compose modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md#section_nws_1rs_rfc)**

Enable agents to initiate a comment, work note, or email in the activity stream and then open the text in a modeless dialog. This feature is available on the following record pages:

    -   Front-line case page
    -   CSM default record page
    -   CSM Interaction record page
    -   CSM voice interaction record page
    -   CSM centered chat interaction record page
    -   Email interaction record page
-   **Activity Stream enhancements**
    -   Activity Stream layout now automatically adjusts to your device \(laptop, tablet, or mobile\). Hidden content is indicated by \(...\) for better readability.
-   **[Lookup component on CSM Configurable Workspace record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-record-page-lookup-component.md)**

Use the Lookup component to look up and link a contact and then verify the contact. The Lookup component replaces the Lookup and Verify component on the CSM Configurable Workspace record pages.

-   **Hide inbox after item selection**

The Inbox panel collapses after selecting an inbox item, enabling agents to see more of the screen and focus on the interaction.

-   **Multi-form controller support**

Supports having two forms on a record page.

-   **Real-time notification count updates**

Updated the bell icon behavior so the notification count accurately reflects the number of unique, unread notifications in real time, eliminating duplicate increments.

-   **[Customer History enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-history-component-features.md)**

Use the following enhancements to control grouping, appearance, and refresh behavior in customer history:

    -   Enable time grouping by month or quarter: A new property enables selection of time grouping as monthly or quarterly \(Q1-Q4\) in date filters.
    -   Customize feed appearance: Admins can configure feed icons along with their background colors using a property that offers predefined color options.
    -   Display activities by updated date: A new property enables feeds to surface activities based on the last updated timestamp in Customer History.
    -   Dynamic refresh updates: Customer History feeds now refresh automatically, but only for records in the Customer History activities table and within the current context \(for example, Contact\). Other tables and parent records are not included.
    -   Introduced a new search icon that lets agents show or hide the search bar with a click.
-   **[Improve discoverability of Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md)**

Use the following updates to improve the visibility of Recommended Actions across key CSM pages:

    -   Set Recommended Actions as the default first tab in the contextual side panel to provide agents with instant access to recommendations without switching tabs. This change applies to the following pages:
        -   Front-line case page
        -   CSM default record page
        -   CSM Interaction record page
        -   Email interaction record page
        -   CSM voice interaction record page
        -   CSM centered chat interaction record page
    -   Load Recommended Actions asynchronously to keep the UI responsive while recommendations load.
    -   Enable agents to send relevant KB articles through SMS during voice interactions and messaging-type interactions.
-   **[Default recommendations for Pro customers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md)**

Recommendations are now delivered by default for Pro customers when either the Task Intelligence for CSM or the Now Assist for CSM plugin is installed. Agents can view contextual recommendations under the **Suggested Actions** tab, such as similar cases and open incidents, when the case meets the predefined criteria. Agents can link or copy resolutions directly into the current case.

-   **[Resurface special handling notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/c_OnScreenAlerts.md)**

Display the special handling notes at any time by selecting  Special handling notes  from the More actions menu on the case record action bar. This action is now available on records from the following tables:

    -   Account
    -   Asset
    -   Contact
    -   Incident
    -   Product Model
    -   Work Order Task
This applies only to records where special handling notes are configured.

-   **[Information session tab enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-workspace-chat-session-tabs-configure.md)**

Use the following changes to enforce permissions and improve usability of the **Session** tab:

    -   Restrict access to unauthorized users with error messages and validate role-based permissions.
    -   Auto-save admin updates to timer and color changes in real time.
    -   Display workspace settings only after the Session tab is enabled.
-   **[Configure Alert Dismissal settings at experience and alert level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/auto-dismiss-alerts-in-csm-configurable-workspace.md)**

Use the following settings to control alert dismissal:

    -   Set alerts to auto-dismiss or require manual dismissal.
    -   Configure alert behavior globally or according to alert.
    -   Reduce alert overload while supporting accessibility standards, which helps agents focus on critical alerts.
-   **[ServiceNow Link Manager is available on the Google Chrome, Microsoft Edge, and Mozilla Firefox plugin store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-workspace-snow-link-manager.md)**

Streamline tab management and reduce browser clutter with ServiceNow Link Manager:

    -   Automatically consolidates new ServiceNow related tabs into an existing open ServiceNow tab.
    -   Provides cross-platform support.
    -   Enables agents to share record links, such as cases, through platforms like Gmail, Microsoft Teams, Microsoft Outlook, and other web tools integrated with ServiceNow. These links open using ServiceNow Link Manager, ensuring the record loads in the correct workspace and context.
    -   Provides a user-friendly interface that is easy to enable and turn off directly from the extension settings in the respective browser.
-   **[Follow records to receive notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-default-record-page.md#section_follow_action)**

Select the **Follow** action to receive notifications when comments or work notes are added to a record. The Follow action is available in the More actions menu on the [Front-line case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md) and the [CSM default record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-default-record-page.md).

-   **Information icon**

Select the information icon on a reference field to display additional information about the record in a pop-up window. Starting with CSM Configurable Workspace Bundle version 5.0, the information displays in a pop-up window with an option to open in a separate tab instead of opening directly in a separate tab. This change applies to the following record pages:

    -   CSM Front-line case page
    -   CSM default record page
    -   CSM Interaction record page
Users can use Cmd+click \(Mac\) or Ctrl+click \(Windows\) when selecting the information icon to use the previous behavior.


</td></tr><tr><td>

App Engine Studio

</td><td>

-   **[Granular configuration admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/aes-personas-roles.md)**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Separate App Engine Management Center release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/aemc-rn.md)**

The App Engine Management Center \(AEMC\) release notes now appear separately from the App Engine Studio release notes because you can use AEMC to manage app development for apps built in App Engine Studio, Creator Studio, and ServiceNow Studio. For information about AEMC, see [App Engine Management Center release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/aemc-rn.md).


</td></tr><tr><td>

Application Manager

</td><td>

-   **[Unlicensed application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/available-for-you-app-mgr.md)**

In addition to details about applications that are already licensed, the "Available for you" tab of the Application Manager now includes information about applications that haven't been procured from the ServiceNow Store yet.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **[Configure maximum rows in related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/avm-configuring.md)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-rt-states.md)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Enhanced SSO login and logout experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/c_MultipleProviderSingleSignOn.md)**

Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-with-fido.md)**

Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/oauth-inbound-and-outbound.md)**

Configure OAuth integration that includes the following enhancements:

    -   You can provide a maximum client secret length up to 4096 characters to meet security requirements of the third-party systems.
    -   You can provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
    -   You can request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\). It also supports RS256, RS384, RS512, HS256, HS384, and HS512.
    -   You can customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

</td></tr><tr><td>

Build Agent

</td><td>

-   **[Improved checkpoint and update set management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ba-conversational-change-log.md)**

Build Agent handles checkpoints and update sets differently in the following ways:

    -   Checkpoint 0 no longer creates an update set.
    -   Checkpoint 1 is the base update set for all subsequent changes.
    -   Update sets use human-readable naming.
-   **[Enhanced semantic metadata search tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/build-agent-tools.md)**

An updated semantic metadata search tool improves performance replaces the previous semantic search tool.


-   **[Build Agent version parity for PDIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

Personal development instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **[Updated interaction limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
**Note:** Limits are per-instance, not per-user. Only submitted prompts contribute to the limit. Plan approvals aren't counted.


-   **[Support for global scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-build-agent.md)**

Build apps and metadata in the global scope.


</td></tr><tr><td>

Case management for CSM

</td><td>

-   ****

Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity. Sharing task plant template features include:

    -   Access control: Users can now provide access to task plan templates at various levels, including user, group, and service organization.
    -   Ownership Management: The Owner or an Admin can change the ownership of a Template by updating the Owner field.
    -   Global template: Task plan templates can be marked as global, making them visible to all users with read access.
    -   Form and List Layouts: Admins can view and edit form and list layouts for sharing, displaying all relevant fields.
    -   Notifications: In-app notifications are sent when access is granted, Selecting the notification opens the shared template directly.
-   **[Task plan template configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/task_plan_template_configurations.md)**

Admins can create configurations for task plan templates that pre-fill information when creating a new task plan template.


-   **[Filtering service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-service-definitions.md)**

Enable agents to filter the service definitions that are shown on the service selector in the following ways:

    -   By user, role, group, or agent
    -   By entity critera such as location, customer level, or related entities
-   **[Case lines for Case Management - Add multiple entitlements to case lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-case-mgmt-case-lines.md)**

View the available entitlements on a case line and associate the multiple entitlements to that case line. Available entitlements are associated with the contracts and entitlements that are purchased by the customer.

-   **[Targeted Communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/targeted-comm-publication-workflows.md) and [Case Digests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-service-case-digests.md#section_ast_r2k_qfc) workflows**

Legacy workflows for the Targeted Communications \(com.sn\_publications\) and Case Digests \(com.sn\_csm\_case\_digest\) applications have been migrated to low-code flows in Workflow Studio. The functionality of the flows remains the same.

-   **[Classifying sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/dps-data-privacy-overview.md)**

Fields in the Customer Service Management and Targeted Communications tables are mapped to the Data Privacy data classes. For more information, see the [Data privacy overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/dps-data-privacy-overview.md) topic in the ServiceNow® Platform Security documentation.

-   **Deny-Unless ACLs implemented on CSM tables**

Deny-Unless access control lists \(ACLs\) were implemented on CSM tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only authenticated users can perform read, write, delete, or create actions on these tables. For more information about Deny-Unless ACLs, see the [Deny-Unless ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/acl-denial-behavior.md) topic in the ServiceNow® Platform Security documentation.

-   **[Customer Service Case Types moved from family to store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-service-case-types.md)**

Starting with the Zurich release, the Customer Service Case Types application \(sn\_csm\_case\_types\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Service Case Types store app.


</td></tr><tr><td>

Change Management

</td><td>

-   **[Propose a standard change template in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/propose-standard-change-sow.md)**

As a user with the itil role, you can create a standard change template proposal in Service Operations Workspace.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/config-code-signing.md)**

You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[My Work enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/my-work-in-cwm.md)**

Track all your work from one place using the enhanced My Work in CWM. My Work now supports all ServiceNow task records-such as incidents, changes, and requests-whether they originate in CWM or outside, giving you a unified view of everything assigned to you. This helps you stay on top of overdue or open tasks and improves on-time delivery.

Additionally, the Item type filter has been refined to show all CWM tasks \(including custom ones\) grouped under a single category, instead of listing every CWM task type individually. You’ll also only see task types in the filter that you’re actually assigned to, reducing clutter and making it easier to filter what matters.

-   **[Enhancements to tables in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/cwm-docs.md)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.
    -   Select multiple cells of a table using the mouse device or by pressing **Shift+ one of the arrow keys** on the keyboard.
    -   Delete content from multiple cells using the **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy content from one cell and paste it to multiple cells.
        -   Copy content from n number of cells and paste it to another set of n number of cells.
        -   Copy content from multiple cells and paste it as a new table in an empty block on the page.
-   **[Enhancements to CWM Board templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/templates-in-cwm-for-spaces-boards-and-docs.md)**
    -   Save template: While saving a Board as a template, choose between saving the current view or all shared views. You can see the number of Board views and custom task types that are included in this template.

These details are displayed in the Template Center, where you can select a template that best meets your team's needs.

    -   Apply template: While applying a Board template, you can see the number of Board views and custom task types that you get if you apply this template. The Board views drop-down list lets you switch between views and provides information on the type of views that are enabled in this template.

Only those custom columns that are part of these views are brought over when you apply this template.

-   **[Collaborating with Spaces in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/cwm-spaces.md)**

When a user is added to the **Assigned to** field of a CWM task but doesn't yet have access to the Space, the email notification requesting access is sent only to the Space owners. This way, there's less email clutter for all the Space users because notifications are sent to only those users who need to know this information.

-   **[New columns for CWM tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/agile-sprint-planning-in-cwm.md)**

Every task within a CWM Board has new columns called Sprint and Story points. You can use these columns if you choose to plan any task into Sprints. These columns are available on every type of work item, including the items that are brought into the Board through Connected work.

-   **[Changes within CWM Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/cwm-docs.md)**
    -   Open the keyboard shortcut panel:
        -   macOS: Cmd + Option + K
        -   Windows OS: Ctrl + Alt + K
    -   Images can be resized after inserting them within a table cell.
    -   The page name can be updated by editing the name and clicking anywhere on the Doc.
    -   Moving content blocks to within a numbered list or deleting a list item from a list automatically adjusts the list numbering.

</td></tr><tr><td>

Common Core

</td><td>

-   **[States in the entity based record access update utility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/eba-configuration-states.md)**

A new Preview state has been added to the record access update utility life cycle. You can now review the estimated number of impacted records before you apply the restrictions. This step helps you to validate the selected scope, assess potential impacts, and make adjustments, if needed. It also adds an extra layer of control and reduces the risk of unintended access changes.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **[Browser warning for unsaved changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/config-browser-warning-unsaved-changes.md)**

Configure a browser warning to alert you of unsaved changes when you navigate away from a page using the back or forward buttons.

-   **[Record List component bundle enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20list/overview)**

Configure these enhancements to the Record List component bundle in UI Builder:

    -   Select **Related** list as a list type option.
    -   Switch between the standard view and gallery list, which displays list items as cards.
-   **[Export lists to Google Sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/exporting-lists-google-spreadsheets.md)**

Export your lists to Google Sheets directly from the Export menu.

-   **[Live updates for lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/live-list-updates-configurable-workspace.md)**

Configure live updates at the list page level without affecting other lists in your Configurable Workspace.

-   **[AI filter assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/use-ai-filter-assist.md)**

Convert everyday language into an encoded query with AI filter assist.

-   **[Predicate Builder component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-predicate-builder/uib-setup)**

Configure these enhancements to the Predicate Builder component in UI Builder:

    -   Use the Predicate Builder for all list types.
    -   Set up a read-only version of the Predicate Builder to display all conditions without users editing them.
-   **[Form component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/form%20record%20page/uib-setup)**

Configure these enhancements to the Form component in UI Builder:

    -   Display Boolean fields as a toggle.
    -   Add an indicator that marks unsaved fields after any changes.
    -   Wrap field labels instead of truncating them.
    -   Change field-level configurations from field context menus displayed as a gear icon beside every field label.
    -   Choose whether related lists load with the form, after the form, or on demand.
    -   Hide the related list header when the last record is removed.
    -   Choose to display field labels beside its value or stacked vertically.
    -   Suppress special handling notes and notifications from secondary forms on a page.
-   **[Personalize Form menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/hide-personalize-form-menu.md)**

Customize which fields display on a form with the Personalize Form menu in the form header. Use system properties to hide the Personalize Form menu or change the roles with access to the menu.

-   **[Format string fields with guidance text and inline validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/format-regex-pattern-string-fields.md)**

Set up guidance text to display in string fields with format requirements such as account ID, SSN, or SIN. Use regular expression inline validation to display an error message if input values are incorrect.

-   **[Advanced view rules configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-advanced-view-rules-forms.md)**

Use client scripts to set up view rules configurations.

-   **[Activity Stream Compose component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-activity-stream-compose-connected/uib-setup)**

Configure these enhancements to the Activity Stream Compose component in UI Builder:

    -   Hide the rich text editor toggle for your workspace without affecting other experiences.
    -   Rename and reorder Emails, Work notes, and Comments tabs.
    -   Annotate new activities to make it easier for you to find unread emails and messages.
-   **[@mentions for the email composer](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/shared-components/now-email-client-composer-connected/overview)**

Configure @mentions in UI Builder for the Email composer and Email composer \(mini\) components, enabling you to add an email recipient by using an @mention in the email body.

-   **[Digital signature and encryption in the email composer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/config-email-digital-signature-encryption.md)**

Send emails with a digital signature that verifies you as an authentic sender and an email encryption that certifies authentic recipients.

-   **[Custom attachment layout](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-record-common-attachments-connected/uib-setup)**

Configure a custom layout mode for the Attachments component in UI Builder. Customize the maximum file size, file types, multiple file uploads, and preview modal.

-   **[Adding the Now Assist icon to action buttons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/create-da-buttons-now-assist-icon.md)**

Use declarative actions to create buttons with the Now Assist \(\[Omitted image "icon-ai-sparkle.png"\]\) icon and hover animation.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Remediation task rule execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Optimized Tenable.io Compliance Results ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/tenable-io-integrations-list.md)**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/qualys-rest-messages-cc.md)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **Optimized Tenable.io Compliance Results ingestion**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is deprecated and replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Configure Tenable test result granularity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/cc-tenable-tr-granularity.md)**

Starting with v15.6.1, you can configure the granularity of Tenable Configuration Test Results \(CTRs\) to split results into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure Qualys Test Result Granularity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/cc-qualys-tr-granularity.md)**

Starting with v15.4.3, you can configure the granularity of Qualys Configuration Test Results \(CTR\) in configuration compliance and split CTRs into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure maximum rows in related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-max-rows-rel-list.md)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-rt-states.md)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v7.6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/cmdb-workspace.md)**
    -   On the Published policy tile on the Data Manager policies page, the policies list view now shows the scheduled job that is associated with the policy and the user that the policy runs as.

For more information, see [Create a CMDB Data Manager policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/data-manager-create-policy-wrkspc.md).

    -   Instead of the system automatically setting the **run as** attribute of the scheduled certification and attestation jobs to be the user that authored the policy, you can now set a specific user that adheres to the policies and regulations in the organization. Configure the default values for the run as user and user accounts available for run as assignees for auditing purposes when it’s important to know who initiated the changes.

For more information, see [Components related to CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/components-cmdb-data-manager.md).

    -   For certification and attestation policy tasks, choose how to assign tasks in cases where a specified task assignment field is empty for a target CI. Specify a user or a user group to assign such tasks to, or create the tasks without assigning them. An administrator can later review and assign those tasks.

For more information, see [Create a CMDB Data Manager policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/data-manager-create-policy-wrkspc.md).

    -   View the closed tasks in the My Work view in CMDB Workspace. Select the Closed card in the Task status tile to review the \(in read-only mode\) details for tasks that are in the Closed Complete, Closed Canceled, Closed Incomplete, or Rejected state.

For more information, see [My Work view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/cmdb-workspace-govern-view.md).

    -   New CIs in the Create CI experience no longer have their **Operational status** attribute set. The new **CI Operational state** attribute appears on the Additional attributes page of the Create CI experience. Setting it to any value is optional.

For more information, see [Create a CI manually in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/create-ci-manual-cmdb-workspace.md).

    -   The itil user role now contains the sn\_cmdb\_user user role and no longer contains the sn\_cmdb\_editor user role. As a result, the following functions that were accessible to itil users now require the sn\_cmdb\_editor user role:
        -   Create and delete the operations that are related to CMDB 360 queries.
        -   Access the CMDB Retirement Definitions module by navigating to **All** &gt; **Configuration** &gt; **CMDB Retirement Definitions**.
        -   Access the Create CI quick link on the Home view of CMDB Workspace.
-   **[Containment in the itil user role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/installed-with-cmdb-workspace.md)**

In zBooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

-   **[Constraints when deleting a CMDB Data Manager retirement definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/data-manager-manage-ret-def-wrkspc.md)**

The same constraints that exist when deleting a retirement definition in CMDB Workspace now apply when directly accessing the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table:

    -   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
    -   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.
-   **[Prioritize using IRE identification rules for uniquely identifying CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/ire.md)**

Configure the system to prioritize the use of IRE identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** fields. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to control this behavior, see [Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/properties-id-reconciliation.md).

-   **[Run a query in an enhanced execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/config-query-builder-engine-mode.md)**

Set the execution mode for a saved CMDB Query Builder query to run using an enhanced query execution engine, which is designed for improved performance and scalability.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[New role required for the Create configuration item agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-ci-creator.md)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Configure maximum rows in related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-max-rows-rel-list.md)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[New Authorization Documents tab for ATO reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/prepare-auth-pkg.md)**

Access all Authority to Operate \(ATO\) artifacts reports from the new **Authorization Documents** tab available in the Authorization Package.


-   **[New CAM System Properties page for administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/cam-components-installed.md)**

Access the new CAM **System Properties** page to enable administrators to configure various system properties.

-   **[Track package progress with the Ageing of Packages widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/cam-ws-home-page.md)**

View the duration that a package stayed in each step, like Prepare, Categorize, Select, Implement, Assess, Authorize, and Monitor, using the Ageing of Packages widget.

-   **[Set Next Engagement Date for Automated Audit Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/prepare-auth-pkg.md)**

Enter the **Next engagement date** to automatically generate the audit engagement on the specified date.


</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Contract family hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-linking-parent-child.md)**

The Related contract requests tab displays the complete contract family hierarchy for the open contract request, including parent, sibling, and child records at all levels. A visual indicator highlights the contract request that is currently open within the hierarchy. Previously, only the immediate parent and direct children were displayed.

-   **[Supporting document upload in additional contract request states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-ss-add-suprt-doc.md)**

Upload multiple supporting documents in a single action from your computer, activity stream, or external storage from the Supporting Documents tab. You can attach supporting documents in the Awaiting Approval, Awaiting Signature, and Contract Signed states, along with the previously supported Draft, Work in Progress, and Awaiting Review states.

-   **[Signatory status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signatory-roles.md)**

The signatory statuses in a contract request have been updated. Pending Signature is now Pending, Signed is now Completed, and Signature Declined is now Declined. The Not started status is unchanged.

-   **[Send contracts for signature using Adobe Sign without signing in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-nss-review-request.md)**

Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-compare-docs.md)**

Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-addin-add-clauses.md)**

See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-set-ext-app-config.md)**

Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.

-   **[Select contract type while initiating a third-party contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-initiate-non-ss-cnt.md)**

Specify whether a contract request is for a single contract or multiple contracts. For single contracts, you can select the type of contract document.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/snlc-submit-request-tpc.md)**

Automatically classify a contract request as single contract type or multiple contracts type based on single or multiple contracts when creating a third-party contract review request from Employee Portal. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-add-clauses-doc-tmplt.md)**

Define clause conditions on fields and variables of a table that isn't directly linked to the contract template table. The condition determines when the clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-append-data-table.md)**

Insert additional data from the related table fields into the dynamic tables of a contract using scripts. Display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-create-ct-word-addin.md)**

You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

-   **[Configure dynamic tables for contract template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-addin-table.md)**

Set up contract templates on the Contract Request \[sn\_cm\_core\_contract\_request\] table to reuse the template across business units. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

Additionally, the **Table** field has been renamed **Lookup table**. You can select the table from the data that is populated into the contract document.

If the template isn't based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Copy fields from parent request to contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-copy-fld-frm-parent.md)**

Automatically copy the required fields from the originating business unit record to the contract request when it's initiated.

-   **[Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-signature-workflow.md)**

Wet signature requests are sent one signatory at a time, starting with the first signatory in order, rather than to all signatories at the same time. Signatories can be changed even after the signing process has been initiated. When a signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Modify signatories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-pause-signature.md)**

Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Resend signature request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-resend-sign-req.md)**

Enable contract fulfillers to manually trigger a signature request when needed instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configuring signatories in Contract template using Microsoft Word add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-config-sign-addin.md)**

Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\) instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Deleting questions from unpublished forms removes the record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/creator-studio-delete-forms-questions.md)**

When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


</td></tr><tr><td>

Customer self-service for Sales Customer Relationship Management

</td><td>

-   **[Order exception support for quantity and shipping location requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/request-order-changes-now-assist.md)**

Enable customers to request quantity changes and shipping location updates for existing orders, in addition to expedited delivery, through the chat assistant on the Business Portal.

-   **[Voice assistant intake for order exception requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-order-mgmt-voice-aiagent.md)**

Enable customers to submit expedite, quantity, and shipping location requests through the voice assistant. The voice assistant captures the request and creates an order case for the order case agent to resolve it in the CSM Configurable Workspace.

-   **[Scripted extension points for order exception checks and quote thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/create-atp-api-call.md)**

Provide administrators pluggable scripted extension points so they can integrate the chat assistant with their inventory, ERP, and quote systems for delivery availability, quantity validation, shipping location validation, and quote threshold evaluation.

-   **[Consolidated extension point for order exception feasibility checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/create-atp-api-call.md)**

Provide a single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) for the manage order operations chat assistant to validate delivery availability, quantity, and shipping location feasibility for order exception requests. This extension point replaces sn\_ord\_ops\_aias.orderExpeditionCheckEP, which previously handled only available-to-promise \(ATP\) checks for expedited delivery.

-   **[Account and contact populated on interaction records for order exception chats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/view-interactions-on-order-case.md)**

Provide live agents with the customer's account and contact details on the interaction record when an order exception chat is handed off from the Business Portal. The Account and Contact fields are auto-populated on the interaction record during the virtual assistant conversation, so the live agent immediately sees the customer context, and the chat summarization feature can summarize the conversation by using those details.

-   **[AI-generated chat summary for live agent handoff](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/resolve-invoice-case-now-assist-agent.md)**

Provide human agents with an AI-generated summary of the customer's prior virtual assistant conversation at the point of live agent handoff, replacing the full conversation history to accelerate context understanding and improve agent productivity.

-   **[Order line quantity validation for invoice disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/configure-invoice-quantity-check-ep.md)**

Provide the invoice dispute support assistant AI with an additional validation source for quantity disputes by checking order line quantities when sold product records are unavailable, supporting scenarios such as new orders, non-serialized products, and consumable services. The assistant auto-approves eligible disputes and escalates to a human agent only when order data is ambiguous or missing.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Enhancements to the declarative responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/declarative-resposibility-framework.md)**

Introduced several key improvements to enhance the flexibility and usability of the declarative responsibility framework:

    -   Enabled responsibility access configurations to support more granular access control.
    -   Updated the data model by adding new fields and renaming select field labels for improved clarity.
    -   Refreshed associated forms and lists to reflect the latest framework updates.
-   **[Updated account manager responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/list-of-reponsibilities-provided-with-base-system.md)**

Enhanced access configurations for account manager responsibilities by creating a unified entity that defines access based on record and role for more consistent and streamlined access control.

-   **[Managing account addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/associate-address-account.md)**

Manage account addresses by associating locations with accounts where the Update access is granted to confirm tracking of address information and support account management.

-   **[Updating location records associated with account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/delete-address-location-form.md)**

Restricts users from updating a shared location record unless they have the Update access to all associated accounts, confirming location details can only be modified with the necessary permissions across every linked account.

-   **[Delta price enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/sold-product-form.md)**

The following are enhancements added in Delta pricing:

    -   Added pricing fields that reference sales agreements and captures base prices on sold products to verify consistent pricing during modifications, such as quantity changes or attribute updates. New fields are added to enhance the traceability for subscription-based products.
    -   Added columns to the Sold Product base table. Use the Split from and Split from root to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.
-   **[Install base data model enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/create-install-base-item.md)**

Improve traceability and product life cycle management with the **Install Base Identifier** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Access control improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/sold-product-form.md)**

Provide hierarchical access to Install Base items for location managers and staff to manage assets sold by or associated with their service organizations.

-   **[Entity configuration and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/entity-configuration-and-mapping.md)**

Gain precision in sales entity setup with three new columns in the Lead to Cash Entity Definition table: Filter Conditions, Enable Post Processing, and Post Processing Script. These columns enable targeted data filtering and post-processing logic execution.

-   **[Explore partial sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/about-partial-sync.md)**

Partial sync processes the data sections you specify instead of the entire structure, significantly improving performance and reducing resource consumption.

The partial sync enhancement includes improved error handling that provides clear, actionable error messages when mandatory fields are missing from synchronization requests.

-   **[Setting up products and available services at a business location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/products-services-at-bus-loc.md)Support for service-related capabilities in business locations**

Enable service-related capabilities for business locations by activating the optional Customer Service Case Types \(sn\_csm\_case\_types\) plugin.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[Full scan support added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/configure-data-discovery-jobs.md)**

Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/data-discovery-attachment-scanning.md)**

Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/configure-data-discovery-patterns.md)**

Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


-   **Key word matching**

As part of key word matching when discovering sensitive data using regex, more precise data pattern matching has been implemented, using full strings of text. This may require customers to add more specific variants of keywords to achieve the same level of discovery precision as prior platform releases


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Support for MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/playbook-enter-github-instance-details.md)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/sc-github.md)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-reference-error-messages.md)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/installed-with-dev-ops.md)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-commits-release.md)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-config-change-details.md)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-dev-ops-extensions-azure.md)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devops-jfrog-connect-workspace.md)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/servicenow-custom-actions-for-gitlab.md)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/run-health-scan-check.md)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dev-ops-change-acceleration.md)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.

-   **[Jira authentication with 3LO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/connect-a-jira-tool-using-oauth-2-0-with-3lo.md)**

Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

-   **[Bitbucket Cloud basic authentication using API token with scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/bitbucket-integration-dev-ops.md)**

Connect to Bitbucket Cloud using Basic Auth by providing the email address and API token with the required scopes for your Bitbucket Cloud account as app password has been deprecated by Bitbucket.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **[Upgrade enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/dev-sbx-clone-upgrade-info.md)**

Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[Use DEX Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/use-dex-desktop-exp.md)**

By default, the Desktop Assistant home page now has two sections: My resources and Quick links. My resources includes Device health check and Network test cards, while Quick links includes Employee Center and Outages cards.

-   **[Modified Devices page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dex-workspace-devices-tab.md)**
    -   The device view is now optimized and segregated into two tabs based on the user persona. The **All devices** tab is for DEX operators, and the **Devices by ACC status** tab is for DEX operators and DEX admins.
    -   The application performance tab in the Device page has been enhanced. Filter performance for installed apps and web apps by date and time, and view the performance metrics for the last seven days.
    -   Access the performance page to view the performance and details of both installed and web applications.
    -   Filter the active devices to view only the devices that were active in the last five minutes.
-   **[Updated landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dashboard-cards.md)**

The world map in the **Devices** section on the DEX landing page now shows the devices list instead of users list. The Impacted Devices card now shows the count of impacted users based on the alerts of both the devices and the applications running on that device.

-   **[Updated users link reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/devices-form.md)**

The user link now redirects to Users page in Service Operations Workspace.

-   **[Changed device alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/user-health-card.md)**

View alerts for both your device and its applications in the Alerts section of the Devices page.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

Transformed chargeback eligibility rules into technical formulas to determine the eligibility or ineligibility of a selected transaction for chargeback.

New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard by adding new questions and updating existing questions.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Processing Errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

Ineligibility rule conditions have been updated across the RC 4834 Processing Errors sub-categories to align with the latest Mastercard Chargeback Guide. Updated sub-categories include Transaction Amount Differs, Currency Errors, Cardholder Debited More than Once for the Same Goods or Services, ATM Funds Not Dispensed, Charges for Loss, Theft, or Damages, Merchant Refund Correcting Error Resulted in Cardholder Currency Exchange Loss, Improper Merchant Surcharge, Unreasonable Amount, and Cash was not properly provided from a Purchase with Cash Back transaction.

For Currency Errors: A new ineligibility condition has been added. CE is not applicable for ATM transactions \(MCC 6011\) where either the card was issued outside Europe or the terminal is located outside Europe.

For Transaction Amount Differs: The documentation requirements for this sub-category have been updated. For Maestro cards issued in Europe used at terminals outside Europe, no documentation is required. Brazil domestic disputes involving gratuity amounts now have explicit documentation requirements.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Cardholder Disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

Ineligibility rule conditions have been added or updated across the following RC 4853 Cardholder Disputes sub-categories to align with the latest Mastercard Chargeback Guide:

    -   Addendum Dispute
    -   Cardholder Dispute of a Recurring Transaction
    -   Counterfeit Goods
    -   Digital Goods Purchase of USD/EUR 25 or Less
    -   Goods or Services Not Provided
    -   Goods or Services Were Either Not as Described or Defective
    -   No-Show Hotel Charge
    -   Refund Not Processed
    -   Refund Posted as a Purchase
    -   Timeshares
    -   Transaction Did Not Complete
    -   Travel/Entertainment Services Not Provided/Not as Described and Merchant Voucher Issued
New ineligibility rule conditions have also been added for the Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\) sub-category.


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/visa-spoke.md#section_gsl_nw5_vyb)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Connect documents on external cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/upload-versions-external-cloud.md)**

Upload your files directly to an external cloud \(including multiple versions of the document\).

-   **[Permissions for external cloud files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/document-configuration.md)**

Set the sharing permissions on your external cloud files.

-   **[Authenticate personal accounts on external cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/personal-authentication-documents.md)**

Implement personal token-based authentication for an external cloud so that you can verify user-specific access, audit trails, and compatibility with existing and future integrations.

-   **[Connect file extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/upload-versions-external-cloud.md)**

Link any Google Drive file to a document record by selecting a provider and entering the file URL All file extension are now supported.

-   **[HTML to PDF Conversion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/pdf-generation-accessibility.md)**

Specify an image retrieval timeout for HTML to PDF conversion.

-   **[Document classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/share-document-link.md)**

Limit public sharing based on a document's classification.

-   **[PDF generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/pdf-generation-accessibility.md)**

Generate a PDF with accessibility for regulated markets.

-   **[Property value for digital signature using CAC or PIV smart cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/property-value-cac-piv-signing.md)**

Specify the method used to identify and validate the user who has signed the PDF using the property value.

-   **Document summarization**

Use AI to generate summaries for feedback, disclaimers, and usage tracking in PDFs and Microsoft Word files.

-   **[Document Services Framework for Microsoft OneDrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/onedrive-spoke-document-services-framework.md)**

Retrieve the list of files and folders based on the given search query from Microsoft OneDrive.

-   **[Document Services Framework for Google Drive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/google-drive-spoke-document-services.md)**

Retrieve the list of files and folders based on the given search query from Google Drive.


</td></tr><tr><td>

ERP Semantic Mining

</td><td>

-   **[ERP Customization Mining application name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-customization-mining-overview.md)**

The name of the ERP Customization Mining application has been changed to ERP Semantic Mining.


</td></tr><tr><td>

Encryption

</td><td>

-   **[Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/now-platform-encryption.md) API**

Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[Updates to GlideEncrypter functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/glideencrypter-deprecation.md)**

The GlideEncrypter API has been updated to use AES256-GCM encryption via the Key Management Framework. If needed, your instance can be changed to use legacy 3DES encryption, but this task can only be done by ServiceNow support.

-   **[Disable GlideEncrypter on your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/check-3des.md)**

GlideEncrypter can be enabled or turned off using the **glide.security.glideencrypter.allow** system property. This property is unavailable on new Zurich instances, but administrators with the security\_admin role can edit this property in upgraded instances. When this system property is set to **false**, users see this error when attempting to run GlideEncrypter.

    ```
Unsupported call to GlideEncrypter. Details: GlideEncrypter is deprecated and now returns null, please refer KB1320986
    ```


</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **Granular level admin role changes**

Added granular level admin role \(sn\_apm.apm\_admin\) to the following system properties in the Enterprise Architecture Workspace:

    -   glide.ui.sn\_apm\_di\_digital\_interface\_activity.fields- Digital Interface activity formatter fields.
    -   glide.ui.sn\_apm\_di\_digital\_integration\_activity.fields- Digital Integration activity formatter fields.
    -   sn\_apm\_tpm.discoveryModelProductTypesForTPM- Product types of discovery models to consider for TPM software suggestions.
    -   sn\_apm\_tpm.configurationItemsWithSoftwareInstalls- Non hardware configuration items which have software models for TPM discovery process.

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Enterprise Asset Management demo data migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/install-eam-demo-data.md)**

All Enterprise Asset Management demo data has migrated from the Enterprise Asset Management application to either the EAM Demo Data application or Indoor Mapping for Assets application. The EAM Demo Data application contains all Enterprise Asset Management demo data except for indoor mapping-related demo data, which is now included in the Indoor Mapping for Assets application.

-   **[Shipment asset table label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/view-enterprise-asset-shipments.md)**

Starting from the Enterprise Asset Management version 9.1.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/view-enterprise-asset-shipments.md)**

Starting from Enterprise Asset Management version 9.1.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Event Management

</td><td>

-   **Automated regex generation**

Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.

-   **Support for OAuth authentication method in Kafka connector**

Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, enabling you to securely connect and manage access without storing or sharing static credentials.

-   **Support for SCOM 2025 version**

Starting in version 2.17.1, you can now check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.

-   **Group automation enhancements**

Starting in version 26.11.0, group automation now supports grouping by impacted service instances and related log properties, with enhanced test automation details for better visibility. These updates enable more effective analysis of alert correlations and more accurate validation of grouping logic.

The updated Test Automation section provides detailed insights into alert groups, including total alerts, description, grouping category, node, and time, with support for sorting by grouping type.

-   **Validate CI identification in Enrich automation**

Starting in version 26.11.0, you can ensure CI attributes are present in the **Additional info** field of the alert for accurate matching and test CI identification on sample events.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Sitemap support in the Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/webcrawler-external-content-connector.md)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-content-crawl-external-content-connector.md)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/review-crawl-ext-cont-connector.md)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/atlassian-confluence-cloud-external-content-connector.md) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


-   **[Analytics for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/analytics-external-content-connectors.md)**

Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-jira.md)**

The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-microsoft-onedrive.md)**

The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-mspo.md)**

The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-ext-cont-connector-msteams.md)**

The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


-   **[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/webcrawler-external-content-connector.md)**

The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which enables you to specify a custom web source or select a predefined one.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Capacity and Reservations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/configuring-capacity-management.md)**

Use the aggregated schedules of all agents of a territory to allocate resources until a specified cut-off date, after which predicted capacity can be used for bookings. This feature optimizes resource utilization and capacity management for a territory, which helps ensure that business services remain available without overburdening resources.

-   **[Google Maps APIs for  Field Service  capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/google-maps-api-keys.md)**

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you create a Google API key after March 2025, you must upgrade to a supported ServiceNow release version to verify compatibility.

-   **[Smart Assessment for Field Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/configuring-smart-assessment-questionnaire.md)**

Use Smart Assessment for Field Service to do the following:

    -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
    -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
    -   View completed questionnaires in the workspace.
    -   Create follow-up work order tasks from a work order questionnaire based on the responses.
    -   Allow users to retry or replace an attachment if the upload is unsuccessful.
-   **[Field Service Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/setting-up-scheduling-methods.md)**

Migrates data from the Work Parameter table to the Resource Schedule Attribute table for each technician, confirming that work parameters align with the new schedule attributes.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Overview of the Dispute Management workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-management-workflows.md)**

Track the progress of the investigation workflow intuitively with a redesigned user interface that presents each transaction within a dispute case using a clear, process-based layout. This new layout visualizes the distinct stages of the investigation workflow, Investigate, Chargeback, and Closure, which enhances visibility and dispute management efficiency.


-   **[Managing disputes integrated with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/work-on-disputes-integrated-with-mc.md)**

Integrate the Dispute Management workflow with subflows that communicate with Mastercom, supporting an end-to-end dispute life-cycle from raising an initial dispute to final resolution.

-   **[Unified dispute intake experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-intake-overview.md#section_c13_crs_bdc)**

The dispute intake process has been streamlined to provide a clear, intuitive experience for customers and dispute agents, resulting in faster resolution and reduced manual effort. A unified interface now allows cardholders, account holders, and agents to raise disputes for both card and non-card \(ACH\) transactions seamlessly.

-   **[Updated chargeback eligibility questionnaire for May Store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.
Questionnaire questions were updated including RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.

-   **[Updated dispute intake questionnaire for July Store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

New questions have been added to the dispute intake questionnaire to support updated Mastercard chargeback ineligibility rule assessment.

    -   For Goods or Services Not Provided disputes \(RC 4853\): Dispute agents must select the applicable waiver and insurance status for merchandise delivery. Options are: a liability waiver was signed by the buyer; shipment insurance was declined by the buyer; both a liability waiver was signed and shipment insurance was declined; or neither applied. This question is mandatory for dispute agents and is also displayed to cardholders.
    -   For Authorization disputes \(RC 4808\): Dispute agents must identify the current account status. Options include: account closed; suspended or restricted; fraud or compromise; credit-related issue; or account active and in good standing. This question is specific to Mastercard and is not displayed to cardholders.
The following additional changes have been made to existing questionnaire questions in this release:

    -   The **What is the dispute about?** question choice list has been updated: the Multiple Authorization Requests option has been removed from the RC 4808 Authorization list, and Late Presentment has been removed from the RC 4834 Processing Errors list. The following labels have been updated: CAT 3 Devices \(formerly Cardholder-Activated Terminal\); Transit First Ride Risk \(FRR\) and Transit First Ride Issuer Liability \(FRIL\) claims; Installment Billing Dispute-Participating Countries; Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(new\).
    -   Display conditions have been updated for several existing RC 4853 Cardholder Disputes questions — including merchandise return date, date the cardholder first notified the issuer, and whether previous negotiation with the merchant occurred — to reflect the addition of the Cardholder Dispute-Not Elsewhere Classified- United States Domestic sub-category.
    -   For Refund Not Processed disputes \(RC 4853\): The question asking for the date the cardholder first notified the issuer of the dispute is displayed when the credit voucher or transaction receipt is not dated. This question applies to dispute agents only.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **[Added field to Financial transaction table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/fso-core-banking-tables.md)**

Added the **Payment Card** field to the Financial transaction \[sn\_bom\_transaction\] table as part of the Payment card application.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Direct action calls removed from Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md)**

Starting with Zurich Patch 5, the Generative AI Controller \(GAIC\) no longer supports direct action calls in order to support the security requirements that all AI capabilities be protected by Access Control Lists \(ACLs\). To create custom generative AI functionality, use Now Assist Skill Kit instead.

    -   Configure actions in the Generative AI Controller
    -   Generate Content to create AI-generated text responses
    -   QnA to answer user questions
    -   Summarize to shorten long or complex text
    -   Generic Prompt to generate ideas or content on any topic
    -   Sentiment Analysis to identify the sentiment of user input
For more information, refer to [KB KB2716977: Generative AI Controller actions are no longer avaliable for custom workflows](https://support.servicenow.com/kb?sys_kb_id=6460540047ee7a9048cb2920326d4302&id=kb_article_view).


</td></tr><tr><td>

Goal Framework

</td><td>

-   **[Active goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/defining-goals-using-goal-framework.md)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed in the **Goal** and **Parent goal** reference fields across all applicable tables.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Goal system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/components-installed-with-goal-framework.md#section_myd_rzy_fyb)**

Users with the sn\_gf\_goal\_admin role assigned can update goal-specific system properties:

    -   **sn\_gfa.weeklyCheckInDayToMapMonth** - Defines the end day of the week used for mapping weekly target breakdowns to a month. The default value is Friday.
    -   **glide.ui.sn\_gf\_goal\_target\_activity.field** - Enables activity stream for fields of the targets.
    -   **sn\_gfa.target\_breakdown\_decimals** - Sets the number of decimal places displayed for target values when generating target breakdowns. The default value is 2.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Shipment asset table label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/view-hardware-asset-shipments.md)**

Starting from the Hardware Asset Management version 14.0.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/view-hardware-asset-shipments.md)**

With Hardware Asset Management version 14.0.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   **[Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/configure-care-team-portal.md)**

The process for embedding Care Team Portal into your EMR system has been streamlined to enable more efficient launch context configuration.

The portal now supports capturing launch context tokens across multiple launches within the same Hyperspace session when embedding Care Team Portal into Epic's Hyperspace. Previously, only tokens captured from the initial launch were displayed.

The FHIR endpoint is now retrieved dynamically, eliminating the need to embed it directly in the Single Sign-on Script.

-   **[Setting up roles and responsibilities for Healthcare Operations users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/healthcare-life-sciences/cto-setting-up-roles-responsibilities.md)**

Roles and responsibilities have been updated to enable more selective user access.

The following responsibilities were added in Healthcare Operations Core:

    -   Support Department Agent
    -   Support Department Manager
The following responsibilities were renamed in Healthcare Operations Core:

    -   Team Member has become Care Team Member
    -   Team Manager has become Care Team Manager
Healthcare operations users can now be assigned these responsibilities in the Edit member related list within healthcare organizations.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/available-patterns.md)**

Note the following new Pattern improvements using version 1.29.0:

    -   [IBM Hardware Management Console \(HMC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/ibm-hmc-discovery.md): additional fields in IBM Frame \[cmdb\_ci\_ibm\_frame\] and IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\] tables
    -   [Dell PowerMax storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/emc-powermax-discovery-pattern.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [Pure Storage FlashArray](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/flasharray-discovery.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [NetApp Server and Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/netapp-discovery.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [AWS Auto Scaling groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aws-auto-scaling-discovery.md): The relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**
-   **[Employ Tag-based mapping in the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/map-tag-based-services-workspace.md)**

Easily view data and create new tag-based services through an enhanced workspace that includes a dedicated dashboard for managing your tag-based services.

-   **[Name updates in Discovery and Service Mapping Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/red-hat-virtualization-discovery.md)**

Name updates starting with Discovery and Service Mapping Patterns version 1.28.0:

    -   The RHV cloud provider has been changed to oVirt
    -   The RHV MID Server capability has been changed to oVirt
    -   The label for the \[cmdb\_ci\_rhv\_ldc\] datacenter type has been changed from RHV LDC to oVirt LDC
    -   The label for the \[rhv\_credentials\] credential type has been changed from RHV Credentials to oVirt Credentials
    -   The following pattern names have been changed from RHV to oVirt:
        -   From RHV Clusters and Hosts to oVirt Clusters and Hosts
        -   From RHV Discover Logical datacenters to oVirt Discover Logical datacenters
        -   From RHV Virtual Machines to oVirt Virtual Machines
        -   From RHV Discover Manager Instance to oVirt Discover Manager Instance
    -   The following table labels have been changed from RHV to oVirt:
        -   The \[cmdb\_ci\_rhv\_vm\_instance\] table label from RHV Virtual Machine Instance to oVirt Virtual Machine Instance
        -   The \[cmdb\_ci\_rhv\_cluster\] table label from RHV Cluster to oVirt Cluster
        -   The \[cmdb\_ci\_rhv\_ldc\] table label from RHV LDC to oVirt LDC
        -   The \[cmdb\_ci\_rhv\_manager\] table label from RHV Manager to oVirt Manager
        -   The \[cmdb\_ci\_rhv\_object\] table label from RHV Object to oVirt Object
        -   The \[cmdb\_ci\_rhv\_server\] table label from RHV Server to oVirt Server
-   **[Benefit from an updated, curated selection of application service candidates in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/sm-dashboard.md)**

If you have ITOM Content Service installed, you can view an enhanced selection of Application Service Candidates \(ASCs\) that provides more accurate and useful information, with an automatic filter applied to hide irrelevant and non-essential components.

-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/automate-certificates-ejbca-acme.md)**

Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discover-root-certificate-browser.md)**

Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Kubernetes Visibility Agent \(KVA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/acc-kubernetes-visibility-landing-page.md)**

KVA performs continuous discovery to detect changes on resources in a Kubernetes cluster and updates the CMDB with the latest data.

Starting with KVA version 3.11.0, and Informer version 2.5.0, absent namespace CIs aren’t deleted automatically. Create a scheduled job to remove them.

Starting with KVA version 3.11.0, and Informer version 2.5.0, map application services based on traffic connections between the workloads in Kubernetes, by using istio and linked service meshes or the DaemonSet service.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/create-an-http-classifier.md)**

The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.

-   **[Automated Certificate Renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/automated-certificate-renewal.md)**

Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


</td></tr><tr><td>

Identity

</td><td>

-   **[Access analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-analyzer.md)**

Display the Security data filter that is in the **Applied** or **Undefined** status in the Access Analyzer results. Access Analyzer also supports the new criteria in ACLs that is controlled by reference.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


</td></tr><tr><td>

Impact

</td><td>

-   **[The outcome summarization Now Assist skill is now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

This skill is automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[GenAI-powered Root Cause Summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/generative-ai-root-cause-anal.md)**
    -   Use the dynamically generated Root Cause Analysis \(RCA\), which is readily available in the RCA History page. RCA is available not only for alerts but also for the Critical or Warning scenarios of the performance category. This feature is a change to the existing functionality and is delivered dynamically.
    -   The core Root Cause Correlation functionality is being offered under the revised name of Root Cause Analysis to ensure product consistency.
-   **[Artificial Intelligence Readiness Assessment Accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/artificial-intelligence-readiness-assessment.md)**

The content and flow of this Accelerator has been streamlined to provide a clearer assessment and more targeted guidance on your readiness to adopt ServiceNow Generative AI capabilities \(Now Assist\).

-   **[Jumpstart Your ServiceNow AI Journey Accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/jumpstart-snow-ai-journey.md)**

This offering is now available across all packages, and includes clearer guidance on how customers can leverage ServiceNow’s AI capabilities to achieve their organizational goals and objectives.

-   **[Use Guided Setup for Impact Store Application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/guided-setup-impact-in-app.md)**

Use automated registration, the preferred method, to initiate the connection and registration to the Impact Delivery Instance provider instance in one combined step.


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Incident task record behavior changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/create-incident-task.md)**

When an incident task is closed, you can no longer edit the field values in the incident task form. Disabling the fields helps prevent any further updates or modifications to closed incident tasks, reducing audit risks.

-   **[Incident and problem workflow changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/working-incident-record-form.md)**

When a problem record is linked to an incident or multiple incidents, the incident and problem workflow has the following enhancements:

    -   When a fix or workaround is shared from the problem record, an event is added in the activity stream of the incident record as work notes. The event includes a brief description of the provided fix or workaround and a link to the problem record.
    -   When a Known Error \(KE\) article is linked to the problem record, an event is added in the activity stream of the incident record as work notes. The event includes the links to the problem record and the KE article.

</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **Admin role dependency**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[New debugging property for Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/kafka-subscriptions-statistics.md)**

Enable more detailed logging in the Stream Connect logs with the **glide.ih.kafka.stream\_connect.debug** property. This property replaces the **glide.ih.kafka.debug.consume** property.

-   **[Spoke Generator license changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/spoke-builder.md)**

Starting with Zurich, the Spokes list page and Spoke details pages are a part of the ServiceNow Integration Hub Starter Pack. To create a spoke using OpenAPI or Postman collection specification or Now Assist, you need a ServiceNow Integration Hub Professional license in your prod and sub-prod environments.


</td></tr><tr><td>

Interview management

</td><td>

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   **[Schedule an interview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/schedule-interview.md)**

Schedule interviews more efficiently with auto-populated template variables that reduce manual email editing.

-   **[Manage interviews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/manage-interviews-recruiter.md)**

Track applicants' responses to interview invites on interviews records directly.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **[Dynamic artifact detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/lw-dynamic-artifact-detection.md)**

Dynamic artifact detection enables Localization Workspace to identify all translatable content, including your custom artifacts. From version 1.1.0.

-   **[Status synchronization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/lw-status-synchronization.md)**

With status synchronization, you see the same status for your translation request in Localization Workspace as you see for the corresponding project in Localization Framework \(Submitted, In progress, Complete\). From version 1.1.0.


</td></tr><tr><td>

MID Server

</td><td>

-   **[Smart Workload Manager in clusters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_ConfigureAMIDServerCluster.md)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[Enhancements to MID Server logging and JFR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerTroubleshooting.md)**

MID Server logging has been improved with log backups that are preserved in a compressed format on local host with option to fetch to the instance. You can enable JFR logs every four hours and backup JFR files for a set time.

-   **[MID Server has improved performance during heavy discovery load](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerSystemRequirements.md)**

MID Servers no longer have performance degradation due to script include cache misses when using large amounts of worker threads.

-   **[MID Server security logs require 100MB of storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerSystemRequirements.md)**

To store the security logs, MID Servers must be installed on a host with at least 100MB of storage capacity.


</td></tr><tr><td>

Mentoring

</td><td>

-   **[Create a Mentoring program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/create-mentoring-pgm.md)**

The multiple mentoring program enables mentor admins to configure multiple programs that can run at the same time. It enables admins to restrict access based on employee criteria. The multiple mentoring program enables employees to choose and enroll in available mentoring programs, edit their preferences, search for mentors, and send connection requests.

To make a program visible in the Mentoring app, admins need to configure programs with the following information:

    -   Short description
    -   Long description
    -   Employee criteria

</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Enhanced native features in hybrid web screens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/mobile/url-screen.md)**

Enhanced native features in hybrid web screens that support functionality such as native search, quick actions, and customizable welcome messages within hybrid screen launcher or header tabs.

-   **[Enhanced chat push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/mobile/using-enhanced-chat-mobile.md)**

Tap enhanced chat push notifications to go directly to the associated chat.

-   **Promoted actions and suggested topics**

See how Virtual Agent can assist you with suggested actions and topics related to your request.


</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   **Service Workers tab in the Next Experience Inspector**

The **Service Workers** tab displays cache buster details for viewing how service workers impact page performance.


</td></tr><tr><td>

Notifications

</td><td>

-   **[Email digest for multiple target records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configure-email-digest.md)**

The email digest now supports both single or multiple target records within a set time interval.

-   **[Notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-notification-filter-configuration.md)**

Enables admins to control the list of notifications displayed for users under the advanced notification preferences.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Using Now Assist Readiness Evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-now-assist-readiness-evaluation.md)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI- Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

Enable translation settings is now a multilingual service in the Now Assist Admin console.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Set up Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/set-up-na-aia.md)**

Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the LLM for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/select-aia-llm.md)**

The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use Now Assist AI Agents.

The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-use-cases.md)**

The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/incident-trends.md): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generate-work-plan.md): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/service-improvement.md): Admin configurations for additional filters such as category and service have been added.

-   **[Enable UI validation for agentic AI processes and Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-aia-reference.md)**

The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the Now Assist panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-aia-reference.md). This feature is opt‑in and disabled by default.

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-a2a-agent.md)**

The agent to agent flow actions no longer inject an `Authorization: Bearer` header automatically. If your endpoint requires a Bearer token, include the prefix directly in the API Key credential value.


-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-a2a-agent.md)**

Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-use-cases.md)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/incident-trends.md) and [Identify ways to improve service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/service-improvement.md) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generate-work-plan.md) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-evals.md)**

After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


-   **[Updates to platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-use-cases.md)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Generate resolution plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/resolve-requests.md) now takes related records into account when planning next steps. [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generate-work-plan.md) shows suggested next steps and reruns after work is done. [Process images for new tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/images-tasks.md) now links to the created task record upon creation and includes certain metadata from the image.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Platform Request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ticket-status-aia.md)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Understand the Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/understand-na-aia.md)**

The base reflection prompt has been replaced with the ReAct Orchestrator prompt, introducing a Route scheduling mode when an agent needs assistance from another agent during execution.

-   **[Configure Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-ai-agents.md)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Add a Knowledge Graph to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-knowledge-graph.md)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


-   **[Review and complete actions on requests using the Request Status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ticket-status-aia.md)**

The ticket status AI agent has been renamed to the request status AI agent. Request details include an AI-generated summary of the most recent comments on a request. Performance has been improved.

-   **[Confirm your web search tool provider data policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-web-search-ai-agent.md)**

If you select Google as your web search provider for web search AI agent tools, Google uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow AI Platform instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/version-control.md)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-tool-aia.md)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool. After an existing tool is added, you can change it to suit the specific needs of an AI agent.

-   **[Now Assist AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-aia-reference.md)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the Agent properties \[sn\_aia\_property\] table.


</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for App Engine

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for CMDB

</td><td>

-   **[View CI attribute descriptions on CI forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-skill-ci-form-help.md)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-search.md)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[New role required for the Create configuration item agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-ci-creator.md)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Create a CI using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-ci-creator.md)**

Verbal interaction with this feature has improved. Occasionally, you might need to create a CI manually. To help you, the CI creator agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

-   **[Getting advice from Now Assist on CMDB governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-governance.md)**

To help users understand the value of each step in the process, responses now include richer context. The CMDB Governance agentic workflow supports administrators and service owners by improving CMDB data governance. Before starting in on each governance task, the workflow presents the reasons for the task to help you better understand the importance and benefits of the activity. The objective is to ensure that CMDB data is accurate and complete so that users can trust the data.

-   **[Use Now Assist to search the CMDB for CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-search.md)**

Verbal interaction with this feature has improved. Users can now select the CI inline when multiple CIs are returned as matches. A summary of the CI now appears in the conversation. The CMDB search agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information that you provided. The workflow can infer CI relationship data to generate an appropriate query.

-   **[View CI information with the Now Assist CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-agent-ci-summarizer.md)**

Verbal interaction with this feature has improved. You can now view a concise summary of the key CI data by selecting the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

-   ****

Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

-   **[Fix SGC import set issues with the Now Assist SGC diagnosis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-sgc-diagnose.md)**

Verbal interaction with this feature has improved. You can now diagnose a failed import set that is associated with a Service Graph Connector to get a summary of the errors and recommendations for resolving the issues.


</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Configure, Price, Quote \(CPQ\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Automated quality assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/quality-assurance-management.md)**

Enable admins to filter scoring parameters and sort agents and case lists. Admins can sort data, manage filters, and easily organize cases on the dashboard with the new sorting, visibility, and skill management capabilities.

-   **[Activate Now Assist Skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/activate-now-assist-for-customer-service-management-csm-skills_0.md)**

Admins can view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities


-   **[Provide Customer 360 insights agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-service-management-ai-agent-collection-customer-360.md)**

Enhanced Provide Customer 360 Insights with Enterprise Graph and AI agent deep research for richer, more contextual query results.

-   **[Triage cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/case-resolving-use-case.md)**

Multilingual and localization flows in the Triage Cases workflow are now fully supported.


-   **[Configure knowledge generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-knowledge-generation-in-now-assist_0.md)**

Enable users with the **sn\_skill\_builder.admin** role to generate knowledge base articles in Now Assist for CSM by selecting the required input fields from a task record, reducing manual effort and streamlining the knowledge base generation process.


-   **[Configure Sidebar Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-sidebar-summarization-in-now-assist.md)**

Enable customers to generate summaries from the required case and task tables in Now Assist for CSM as default tables can now be pre-selected and locked.


-   **[Changes to Complaint Case AI agent collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/accelerate-complaint-case-handling.md)**

Updates have been added to the Complaint Case playbook to work better with the Complaint Case AI agent:

    -   Triage displays complaint details and enables a human agent to identify and request missing information.
    -   Complaint‑specific case summarization is available directly within the playbook.
    -   Replace research case task activities with case tasks list activity.
-   **[Enhancements in the Sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/use-sentiment-analysis-dashboard.md)**
    -   Sentiment analysis dashboard support has expanded to include interaction records, and positive and negative sentiment drivers have been consolidated into a single Sentiment Drivers view.
    -   The top negative assignment group and number of cases by channel visualizations have been merged into the new Impact Explorer visualization for streamlined analysis.
    -   Widget placement in the Workforce Optimization dashboard has been optimized for accessing insights and trends across interfaces.
-   **[Enhancements in Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/view-trending-topics-dashboard.md)**
    -   The Accounts, Products, Assignment Groups, and Channels graphs have been consolidated into the Impact Explorer card.
    -   Search and pagination have been added to the list header.
    -   The Historical trends resurfacing graph has been added the Trending topics dashboard to show historical trends at a glance.
    -   Trending topics have been expanded beyond the top 10 results to provide deeper insight into emerging patterns.
    -   The trending topics widget has been added in the Workforce optimization dashboard as the **AI insights** tab.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Enhancement in case summarization skill flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/case-summarization-generation-in-now-assist.md)**

The **Define trigger** step has been added to the case summarization flow. This step enables admins to choose between the User Trigger option, where users select a button to generate a summary, and the Automatic Trigger option, where summaries are automatically generated based on specified conditions.

-   **[Enhancement in email reply recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/generate-email-reply-recommendations.md)**

Generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.

-   **[Unified admin experience for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customizing-now-assist-skills.md)**

Skills cloned in Now Assist Admin console can now be edited in Now Assist Skill Kit. This update unifies the admin experience across Now Assist Admin and Now Assist Skill Kit, enabling users to add headers, configure prompts, and manage Now Assist skills in one location. The migration supports case summarization and resolution notes generation.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Display sentiment scale in case list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/analyze-sentiments-in-now-assist-for-csm.md)**

Sentiment scoring has been added to both the case record page and list view across cases, giving agents immediate visibility into the emotional tone of customer interactions. The sentiment scale ranges from very positive, positive, neutral, negative, to very negative.


-   **[Multilingual support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-supporting-info.md)**

Enhanced multilingual support in chat summarization, resolution notes, and knowledge generation. Leveraged native multilingual LLMs for improved fluency and domain specificity, addressing translation inconsistencies across Tier 1 and Tier 2 languages.


-   **[Suggested steps in the Recommended Actions tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)**

View the suggested steps on the **Recommended Actions** tab in the contextual side panel. If suggested steps are available for a case, Now Assist for CSM generates and displays these steps in a card at the top of the **Recommended Actions** tab.

-   **[KB generation skill configuration enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-configuring.md)**

The **Is Template** field on the KB generation skill configuration record is enabled by default. With the skill\_builder.admin role, you can copy or clone the KB generation skill and customize the prompt in the skill kit.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aw.md).

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for FSM

</td><td>

-   **[Create Work Order AI agent performance improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/fsm-ai-agent-use-cases.md)**

The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.

-   **[Removed prompt headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/cust-now-assist-fsm-wot-summarization-skill.md)**

The prompt headers have been removed from the work order summarization skill to support third-party large language models. You can now customize prompts via a hyperlink to the Now Assist skill.


</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/exploring-now-assist-for-financial-services-operations-fso.md#section_ir3_pn5_lbc)**

Disputes intake via Virtual Agent has the following updates:

    -   Questions presented to the user for disputes will follow the dispute questionnaire in the disputes playbook.
    -   Bypass inferring answers to certain questions so that customers provide answers directly, ensuring the correct dispute category and dispute reason are determined.
    -   Supports ACH disputes, Disputes intake via Virtual Agent including submission of the Written Statement of Unauthorized Debt \(WSUD\).
    -   Checks if the disputed transaction is already part of an existing case.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Functional change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-issue-resolver-na.md)**

The resolve HR cases agentic workflow has been broken down into three agentic flows:

    -   [Predict service and transfer HR cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/predict-transfer-hrcase.md)
    -   [Resolve noncritical HR cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-issue-resolver-na.md)
    -   [Resolve critical HR case agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-issue-resolve-critical.md)

-   **[Flow name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-issue-resolver-na.md)**

The resolve noncritical HR cases workflow has been renamed to the resolve HR cases workflow.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

-   **[Now LLM Service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-itom-agentic-aia.md)**

Four AIOps AI agents have been removed from the analyze alert impact agentic workflow because they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[AIOps LEAP rebranding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/exploring-aiops-leap.md)**

AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation.

-   **[Service Operations Workspace \(SOW\) Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/view-and-use-aiops-leap-playbooks-in-sow.md)**

Playbooks appear in SOW module.

-   **[Data Range Display](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/exploring-aiops-leap.md)**

The AIOps LEAP landing page shows analyzed data date range for automation teams to be aware of time-ranges of analysis.


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Customize the change risk assessment answer generator skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-change-risk-assessment-skill.md)**

Control the data that the change risk assessment answer generator skill uses to suggest answers. Create, modify, or deactivate **AI Risk Data Sources** to change which related records and knowledge articles the skill receives. Six data sources are available out of the box, including related affected CIs, impacted services, impacted business applications, service offerings, active change tasks, and outages. To change which change request fields the skill reads, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-assess-quality-change-request-workflow.md)**
    -   Use the assess quality of a change request agentic workflow to rate a change request and get field improvement suggestions. The change quality assessor AI agent rates the request against an active change policy document, suggesting values only for fields the policy defines. If no policy applies, the agent rates the request against similar closed change requests.
    -   The agent scores the short description, description, implementation plan, backout plan, test plan, risk and impact analysis, and justification. Results are recorded in the **AI Change Quality Scores** table.
    -   Track change quality trends in Platform Analytics on the `ai_change_quality_score` table. A line chart shows the average score by month.
    -   To change how the agent evaluates a field, or to assess a custom field, override the `POLICY_EXTRACTION_KEYS` entries in the `ChangeQualityUtil` script rather than the protected `ChangeQualityUtilSNC` script. This ensures your changes remain after you upgrade. Use the `u_custom_field` entry to assess a custom field, and use the `overall_chg_policy` entry to set policies for the whole change request.

-   **[Renaming the Incident assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist.md)**

The Incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

The voice AI demo agents have been renamed as primers.

-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-change-risk-skill.md)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Role masking for change risk explanation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/supporting-information-now-assist-itsm.md)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


-   **[Skills activated by default in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/using-now-assist-for-itsm.md)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Virtual agent topics available as demo data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-va-prebuilt-topics.md)**

The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To Incident|\(DEMO\) Add Comment To Incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close Incident|\(DEMO\) Close Incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark Incident Unresolved|\(DEMO\) Mark Incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve Incident|\(DEMO\) Resolve Incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request.md)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/using-now-assist-for-itsm.md)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization

</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-summarize-case.md)**

Summarization now includes data from extended practice area tables, providing context‑rich summaries for your legal requests and matters.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Operational Sustainability Management Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Order Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Retail Service Management \(RSM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Sales CRM for Telecommunications

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

-   **[Resolve a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)**

Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   **[ppm.ai\_project\_manager\_agent user role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

The agentic workflow, agents, and scheduled jobs are configured to run under the new ppm.ai\_project\_manager\_agent user role instead of the administrator account.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Third-party Risk Management \(TPRM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/auto-complete-suggestion-types-na-ais.md)**

Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/semantic-search-ais.md)**

Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.

-   **[Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-qna-genius-results.md)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md).

-   **[Now Assist Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-catalog-ordering-gr.md)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md).

-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Default large language model provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.


-   **[Improved missing clause detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-NA-review-land.md)**

Missing clause detection in contract revision using the contract analysis skill has been enhanced for accuracy. The setup, configuration, and review experience remains unchanged across all supported workspaces.


-   **[Configure use case mappings for metadata and obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-usecase-mappings-me.md)**

Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)**

The Now Assist powered conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
The conversational search feature does not support searching within contract documents that are scanned PDFs.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Enhanced Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-reminder-agentic-wf.md)**

The manage contract repository agentic workflow has been optimized for enhanced performance. It now utilizes a single agent, the Contract Repository AI agent to extract both contract metadata and obligations from signed contracts, and retrieve required information to calculate the contract reminder date.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **[Extract metadata from signed contracts automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-reminder-agentic-wf.md)**

Use the AI agents in the manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/metadata-extraction-use-case.md)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case is available in the base system.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

The file size limit for uploading a file using the attachment summarization feature is changed from 10MB to 20MB.

-   **[Document Intelligence for Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-document-intelligence.md)**

The document and visual intelligence capabilities used to leverage extraction, question answering, and summarization capabilities for skills created with Now Assist Skill Kit are available to users with the appropriate role\(s\).

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

The page count limit decreases to 20 pages per file for an extraction based on a use case with a table defined.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **Merged skills**

Document data extraction and document Q&amp;A capabilities are available in a single Extract information from documents skill.

    -   The Extract information from documents skill is available in the list of Platform skills in the Now Assist Admin console.
    -   Data extraction and document Q&amp;A capabilities can be set up for the same use case.
    -   Agents can review the AI predictions for the fields, tables, and questions in the same task.
-   **[Document and visual insights AI agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md)**

Leverage added tools that enable the AI agent to display the extracted data and to look up existing use cases or create use cases based on descriptions and document attachments.

-   **[Changes to limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md)**

The limitations set for Now Assist in Document Intelligence properties are updated to support processing larger documents.

    -   DOCX files are supported for information extraction.
    -   The page count limit is 200 pages per file If image mode is turned off for the use case. If image mode is turned on, the page count limit is 10 pages per file.
    -   The file size limit is 20 MB.

</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[Query indicator data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/ai-data-explorer-implementation-checklist.md)**

Get scores from automated indicators in your AI Data Explorer explorations. Only classic automated indicators are supported, not Data Snapshots.


-   **[Explorations not available from visualization or list for unsupported scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/launch-now-assist-explorer.md)**

You can't open AI Data Explorer from a data visualization or list that shows data from a protected scope that is not supported.

-   **[Improvements to generated segments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-segments.md)**
    -   The names of automatically generated segments now include both the module name and the name of the application it belongs to.
    -   Improved logic to join conditions for segments generated from reports and report sources. More complex conditions such as global OR are now supported.
-   **[Query Generation support for Glide Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-unsupported-field-types.md)**

Query Generation now supports Glide List fields on tables.


-   **[Explore data from protected scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/enable-aide-secure-scope-apps.md)**

Provide access to protected application scopes to AI Data Explorer and Query Generation, and you can use data from those application tables in explorations.

-   **[Manual segments are prioritized](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-segments.md)**

Manual segments are re-ranked to take priority over automatically generated segments.


-   **[Improvements to how segments are handled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-segments.md)**
    -   Manual segments are re-ranked to take priority over automatically generated segments.
    -   Prompt changes made to better support manual segments.
    -   More segments are passed to the LLM to increase the chance of the correct segment getting selected. Twelve segments are passed instead of three.
    -   Segments longer than 2000 characters are dropped to prevent context window bloat.
-   **[Customize semantic metadata in configuration tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/customize-semantic-metadata.md)**

Customize semantic descriptions and usage instructions in the table and column configuration tables. Unlike the previous method of editing Entity and Dimension records, these changes can be transferred between instances through update sets.


-   **[View recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/expl-view-recommended-actions.md)**

AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/qg-supported-query-operations.md)**

Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-segments.md)**

Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for modules on domain-separated instances.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Dashboard and data visualization export skill is active by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/export-db-dv-now-assist-panel.md) \(January 2026\)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 5\): If this skill was previously unconfigured, it is turned on automatically \(the skill was never configured and turned on, then turned off again\). If the skill was previously turned on, then off, it remains inactive.

-   **[Query Generation skills are active by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/enable-query-generation.md)**

If the Generative AI Controller plugin is activated, the skills for Query Generation are activated by default. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Greater visibility into the Query Generation process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/ask-expl-questions.md)**

When you call Query Generation from AI Data Explorer or another application, you see each state that the query and response goes through before completing.

-   **[Multi-table source support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/ask-expl-questions.md)**

Query Generation supports related table conditions and dot-walking in queries.

-   **[Get insights and visualizations for Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/create-integrations-applications.md)**

Ask AI Data Explorer information about Workflow Data Fabric data and get insightful responses. You must first add the Workflow Data Fabric tables to the Query Generation Semantic Table Configuration table.

-   **[Use database views in queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/add-table-semantic-layer.md)**

Generate visualizations or ask AI Data Explorer about data kept in database views, like SLA data. You have to add the database views to the Query Generation Semantic Table Configuration table.


-   **[Add tables to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/add-table-semantic-layer.md)**

Choose which tables your users can query with generative AI for data analysis.

-   **[Monitor the health of the Query Generation back end](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/querygen-health-page.md)**

View the state of Now Assist for Platform Analytics LLM, plugins, system properties, components, and dependent products.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Conversational Platform Now Assist skills are active by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

The following Platform Now Assist skills are active by default and no longer visible in the Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/using-now-assist-in-va.md)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/web-search-requestor.md)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/nava-enhanced-chat.md)**

If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Performance improvements in subflows for on-call notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/on-call-new-trigger-engine.md)**

The following performance enhancements are available for on-call notifications when subflows are used:

    -   On-call notifications are sent to multiple channels such as SMS or email simultaneously instead of sending it sequentially.
    -   When the **com.snc.on\_call\_rotation.new\_trigger\_engine** property is set to true, the on-call subflows are processed via the Flow runner queue. The on-call subflows that are marked as High priority are processed faster via a Flow runner queue especially when multiple events are triggered at the same time and are in the process queue.
    -   Reminder notifications are also sent to users when the instance is upgrading.
-   **[Enhanced on-call trigger rules to support subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/on-call-scheduling-subflows-overview.md)**

The on-call trigger rules form is enhanced to trigger a subflow when the trigger rule is executed. You can enable and select a specific subflow for a trigger rule.


</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aw.md).


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **Admin role dependency**

Several new granular admin roles have been added, which enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[Use CMDB groups to add OT context to IT CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/use-cmdb-groups-it-ot-conversion.md)**

When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than one CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/use-cmdb-groups-it-ot-conversion.md)**

The **Automated IT OT Bulk Contextualization - Using CMDB groups** scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **Admin role dependency**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Changes to OM integration with SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/configure-site-project-product-offering.md)**

Use OM integration with SPM to create program, reuse program, create site project and reuse site project in the SPM.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Select whether to drill down to Platform Analytics or Core UI lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/visualization-drilldown-in-config-ws.md)**

Decide whether data view chart interactions for data visualizations on an instance drill down to Platform Analytics or Core UI record lists. This choice applies only on the Platform Analytics experience.

-   **[View usage information in the dashboards library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/dashboards-for-admin-users.md)**

For analytics managers, the dashboard library now contains usage statistics, such as the number of dashboards not viewed in one year and the number of dashboards deactivated for more than three months.

-   **[Export data visualizations from dashboards to PNG and JPEG](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/export-data-vis-from-dboard.md)**

Export individual data visualizations as a viewer to a graphic file.

-   **[Platform Analytics experience is supported even when Next Experience UI is disabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/data-migration-perform.md)**

You can migrate to Platform Analytics even if Next Experience isn’t enabled. Core UI dashboards are embedded in iframes.

-   **[Migration Center changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/data-migration.md)**
    -   Dashboard owners can perform partial migration on their own dashboards.
    -   Geomap migration supported.
    -   Interactive filter check box option.
    -   Export to CSV from lists is supported.
-   **[Data visualizations and filters support Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/workflow-data-fabric.md)**

Perform data analysis on external data fabric sources.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Activate playbooks without a trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer-triggers.md)**

Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **[Implement playbooks that are callable by a scriptable API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/process-automation-designer-triggers.md)**

Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **[Decision activity enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-a-decision-activity.md)**

User experience improvements to decision activities:

    -   In the Board view, select the branch or Start rule icon on a decision activity card to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/add-configure-activity.md)**

Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Improvements to the rationalization process of control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/take-actions-on-the-recommendations-for-similar-control-objectives.md)**

Several enhancements have been made to the rationalization process:

    -   Redesigned the rationalization UI with a reordered layout and highlighted primary actions.
    -   Validations added for deactivated and deleted control objectives. Introduced the “Restart Analyze” option to support reevaluation of recommendations.
    -   Introduced support for Azure OpenAI, Amazon Bedrock, and Google Gemini for recommendations of control objectives.
    -   Updated the Consolidate state UI to show the recommendation panel with retained and accepted control objectives and their associated items.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **Validation logic ensures that Predictive Intelligence can access data tables**

Reduce errors while training Predictive Intelligence models with the help of new validation logic. This validation checks whether your data tables have ACLs \(Access Control Lists\) granting access to Predictive Intelligence.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Processing activity tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/processing-activity-tab.md)**

The revamped Processing Activity overview page provides a unified dashboard that displays key compliance and risk metrics, such as risk scores, compliance scores, and criticality scores. This update makes it easier for privacy managers and analysts to assess the status of each processing activity, track open issues, and prioritize actions.


-   **[Layout for processing activity record view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/processing-activity-homepage.md)**

The vertical layout of a processing activity enables you to see the information in a top-down linear flow. With this layout, you can see the sequential representation of a data processing workflow.

-   **[Privacy management home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/privacy-mgmt-ws-privacy-compliance-manager.md)**

The enhanced Privacy Management home page now has dedicated tabs for Processing Activity, Risk and compliance, Operations, and Privacy Cases. This updated layout helps to improve readability by organizing your reports into clearly defined sections.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Support minor changes to published product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/minor-updates-published-offerings-specs.md)**

Make minor changes to published versions of a product offering or specification, without creating a version. Minor updates include changes such as modifying the product offering display name, description, or product image.

-   **[Configurable product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/som-create-product-offering.md)**

The Create Product Offering form, used when creating product offerings, has two new options. The **Configurable** option indicates that the product offering is configurable and that it can be customized by agents and customers using the CPQ Configurator. The **Enable ramps** option indicates that price ramps can be defined for a configurable product.

-   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/export-import-product-catalog-entities.md)**

Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/export-product-catalog-entities.md).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/import-product-catalog-entities.md).

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Enhancements to Grants Management: Program Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/psds-using-grants-management-playbook.md)**

In the Grants Management: program setup, grant program managers can now add new points of contact for the applicants to the grants program in the Define Program stage. In the Publish Program stage, new fields have been added for program announcement removal. Grants program managers can now set grants programs to auto-remove at a defined date, and set application close to disable new applications from being submitted through the Grants Management portal.

-   **[Enhancements to Grants Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/psds-gmp-using-grants-mgmt-portal.md)**

Enable grant program managers to turn off new grant proposal submissions after the proposal close date. Applicants can no longer submit proposals after the proposal close date, keeping the process on schedule and helping prevent late submissions from being reviewed.

Enable applicants to review and download the results letter and merit review summary \(where applicable\) of their grants application, as well as accept or decline their award, all within the new **Results** tab of the Grants Management portal. Notify constituents about a pending award decision through the portal.


-   **[Constituent Service Dashboard Migration to Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/constituent-services-dashboard.md)**

The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when you load or upgrade to the Zurich release. The dashboard migration to Next Experience enables you to visualize historical and real-time process statistics in role-based dashboards. Access the new dashboard by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


</td></tr><tr><td>

Recruitment workspace

</td><td>

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   **[Get overview of recruitment workload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/recruitment-workspace-oveview.md)**

View all the job requisitions where you're listed as an additional recruiter or recruitment coordinator, on the home page cards and list view in Recruitment workspace. Previously, only the primary recruiter saw these requisitions in Recruitment workspace.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **Administrator role enhancements**

After upgrading to version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

-   **Read-only field enhancements**

Starting with version 21.1.x, the following Regulatory Change Management plugins have security enhancements for read-only fields in this release:

    -   GRC: Taxonomy management \[com.sn\_grc\_taxonomy\]
    -   GRC: Regulatory Change Management integration with RSS Feeds \[com.sn\_grc\_rcm\_rssfeed\]
    -   GRC: Regulatory Change Management \[com.sn\_grc\_reg\_change\]
    -   GRC Case Management Core \[com.sn\_grc\_case\_mgmt\]
    -   GRC integration with Thomson Reuters Regulatory Intelligence \[com.sn\_grc\_int\_tr\]
    -   Regulatory Agency Library \[com.sn\_reg\_body\_mgmt\]
-   **[Tasks widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/list-view-of-reg-alerts.md)**

The overview page of a regulatory alert includes a newly added Tasks widget that enables you to get more visibility into related activities. This widget displays the total number of associated action tasks and change tasks that are linked to the specific regulatory alert. By using this widget, you can assess the level of effort that is required for compliance.

-   **[Workflow of regulatory task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/reg-change-task.md)**

A regulatory task progresses through the following states:

    -   New
    -   Work In Progress
    -   Implementation
    -   Awaiting Approval \(optional\)
    -   Completed
While in the Implementation state, requesting approval is optional. If all associated action tasks are completed, the regulatory task can be closed directly from the Implementation state without requiring additional approval.

-   **[Workflow of source document import task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/reg-change-task.md)**

A source document task progresses through the following states:

    -   New
    -   Ready to Import
    -   Work In Progress
    -   Implementation
    -   Completed.
-   **[Create action tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/manage-reg-action-tasks.md)**

You can create action tasks for a regulatory task when the task is in any of the following states:

    -   New
    -   Work in Progress
    -   Implementation
You can now break down a regulatory task into smaller, manageable components so that you can more efficiently track and execute the required activities. You can plan, assign, and monitor tasks now in a structured manner that supports your compliance objectives and regulatory requirements.


</td></tr><tr><td>

Return Merchandise Authorization

</td><td>

-   **[Enhancements in the RMA case flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/return-merchandise-authorization.md)**

Streamline the sales return process by enabling agents to initiate, track, and close RMA cases for install base items directly within the Agent Workspace. It also bridges the gap between self-service and full support.


</td></tr><tr><td>

Security Center

</td><td>

-   **[Auditor checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/auditor.md)**

The Review Public Knowledge Bases and Review Public Knowledge Base Articles checks use global API calls, so they've been added in the Global scope.

-   **[Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/sec-center-v2.md) Theming for Security Center**

Security Center banners and Cascading Style Sheets CSS elements have been updated to conform to any instance-wide themes you apply.

-   **[Updated first time user experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/sec-center-landing.md)**

Security Center has been updated to provide guidance to understand what the tool can do and how to use it. This redesign is tailored to assist both new and infrequent users of Security Center.

-   **Hardening settings updates**

Updated the Security Hardening tool with the latest Instance Security Hardening Settings baseline V6.

-   **[Security Hardening tool Updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/security-hardening-settings.md)**

The security Hardening tool has been updated to the latest Instance Security Hardening Settings V7.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Incident Response Other Records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-incident-response-other-records.md)**

Add  multiple ITSM incidents, problems, or change requests to a security incident for which multiple IT actions are needed. For more information, see the "Link multiple ITSM incidents" section.

-   **[Modify attachments of a closed security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/t_ClosingSecIncidents.md)**

You cannot modify the attachments of a security incident once the security incident is closed.


</td></tr><tr><td>

Security Posture Control

</td><td>

-   Security Posture Control relies on data from service graph connectors that is populated in the CMDB 360 Data \[cmdb\_multisource\_data\] table. This data is populated only when the glide.identification\_engine.multisource\_enabled system property is set to true. You must have the cmdb\_ms\_admin role to modify property values. To set the property, navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**.
-   The labels on the form view for the mitigation control details record associated with vulnerable item records \(VITs\) have been enhanced for more clarity. These updates make the interface more user-friendly by expanding abbreviations on the form view, such as changing "EDR" to "Endpoint Protection."

</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Using the email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-email-interaction-page.md)**

View annotations for the most recent activity along with a compact email header that includes the subject, sender, and receiver details in the activity stream. Focus on new or unread email messages rather than the entire email conversation.

View or edit the interaction record while drafting an email in a modeless dialog, keeping all relevant information accessible.

-   **[Using Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ci-agent-chat-using.md)**

Leave a chat without ending it for other agents, enabling you to complete your task and exit the chat.

Confirm before closing a chat tab to avoid unintentionally leaving the chat.

Enable multiple agents to add wrap-up codes and comments for a single chat.

-   **[Import queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/import-queues.md)**

Review and update queues imported from a contact center in a post-import page. The post-import page for a queue mirrors the existing post-import pages for skills and wrap-up codes, providing a consistent user experience.

-   **[Interaction Controls Component \(ICC\) call features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/interaction-controls-component-icc-call-interaction-features.md)**

Notify agents when a supervisor is coaching or has joined an active call while monitoring agents directly through the CCaaS system.

-   **[CCaaS callback features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/contact-center-intergration-with-icc-callback.md)**

Callback management has been improved to make handling requests easier for agents. The key changes include:

    -   Equip agents to transfer the callback requests before dialing the call, enhancing flexibility in managing customer interactions.
    -   Enable scheduled callbacks, which help customers to choose a preferred callback time in addition to the existing ASAP option.
    -   Facilitate agents to view the list of queues and other agents for easier callback transfers and efficient customer management.
    -   Capture callback reasons more effectively with the expanded Reason for Call field, which includes additional choice values.
-   **[Unified routing of email interactions via CCaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-email-interaction-customer-service-management.md)**

Email interaction handling has been enhanced to improve efficiency and responsiveness in managing customer communications. The key changes include:

    -   Support external routing of email interactions.
    -   Enable agents to put email interactions on hold while waiting for customer responses.
    -   Notify CCaaS when an interaction is put on hold so that CCaaS can free up the agent's capacity for handling other interactions.
    -   Send automatic email reminders to customers for interactions that are on hold for a configurable period.
    -   Reroute email interactions to available agents when the originally assigned agent is unavailable.
    -   Prevent creating outbound email interactions when emails are sent on top of cases.
-   **[Import queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/import-queues.md)**

Use bulk action to assign service channels to multiple queues simultaneously during queue-import, simplifying queue management for CCaaS integrations.

-   **Portal Data List widget**

The Data List widget now offers more configuration flexibility and supports dynamic, context‑aware view selection. Key enhancements include:

    -   Role‑Based and Guest Views: Use the new role\_based\_views and guest\_view options to define different views for different user roles and for unauthenticated users removing the dependency on a single static view.
    -   Automatic URL Parameter Passing: Pass URL parameters automatically into scripts invoked from Data List instance options enabling admins to build richer, multi‑parameter conditions without extra setup.
    -   Script‑Based View Selection: Use the Data List Condition Script option to choose a view dynamically. Scripts can evaluate URL parameters and other context to determine the most appropriate view at runtime.
    -   Configurable Default Sorting: Define initial sorting behavior using the new sort\_by and sort\_order options letting the users see a meaningful default order when the list loads.

</td></tr><tr><td>

Service Catalog

</td><td>

-   **[A property to delete a draft of catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/save-draft-catalog-item.md)**

Use the property **glide.sc.delete\_draft\_item\_on\_version\_change** to determine whether to delete a saved draft of a catalog item on its modification.

-   **[Dynamic Lookup Choices and Enhanced Table Sourcing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_CreateAVariableForACatalogItem.md)**

Lookup questions are now more flexible and user-friendly. You can effortlessly display choices directly from a specific table field, offering similar ease for select box configurations. Additionally, create dynamic dependent lookups where the choices refresh automatically based on the values selected in other fields on the same form, guiding users to more relevant selections.

-   **[Enhanced Sorting Control for Lookup Fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_CreateAVariableForACatalogItem.md)**

Customize the display order in lookup select boxes, look up multiple choice, and list collector fields with the new **ref\_ac\_order\_by** attribute. This attribute enables options to be sorted primarily by a specified data column, and then by their display label, providing a more logical and predictable presentation for users.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Configure help and order of the remedial action parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/components-installed-with-remediation-fw.md)**

Configure the **Help** and **Order** fields for the remedial action parameters on the Remedial action parameter \[sn\_reacf\_remedial\_action\_parameter\] table if you have the Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\] user role.

-   **[List page enhancements in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/work-incident-list-page-sow.md)**

The list page in SOW has the following enhancements:

    -   The related lists in the **Related records** tab of the SOW record pages, including those within the record pages as well such as Recent Incidents or Assigned Assets, are updated with the record list bundle. This update provides them with the same appearance, functionality, and user experience as the SOW list page.
    -   The related lists in the **Related records** tab of the SOW record pages, including the Multi Record Associator \(MRA\) list, as well as the related lists within the record pages such as Recent Incidents or Assigned Assets, now support the fuzzy count UX page property. You can configure a default value that is applicable to the list for all tables or a value for a specific table such as incident thereby improving the list page performance.
-   **[Dependency view changes for reference fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/view-update-inc-overview-tab.md)**

Selecting the dependency view for the following fields in the incident, problem, change, and request records, opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:

    -   Configuration item
    -   Service
    -   Service offering
-   **[Propose a standard change template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/propose-standard-change-sow.md)**

As a user with the itil role, you can create a standard change template proposal from any change record in SOW.

-   **[Service Operations Workspace access for an on-call shift administrator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/roles-in-sow.md)**

Starting in version 8.2, a user with the rota\_admin role can access Teams, Schedules, and Home pages in SOW.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/javascript-engine-feature-support.md)**

Use additional scripting features, including Promises and Async await, in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[Stream multipart responses with REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_AvailableSystemProperties.md)**

Stream multipart responses rather than buffering responses until complete by default with REST APIs that support the multipart/mixed requests, such as the Batch API. The **glide.rest.serialize.disable\_response\_stream\_buffering** system property controls this behavior and applies only to instances configured with Application Delivery Controller, version 2 \(ADCv2\).

-   **[Additional field types supported in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

The following field types are now supported for use in a configurable workspace:

    -   **datetime**
    -   **email\_script**
    -   **int**
    -   **integer\_time**
    -   **related\_tags**
    -   **user\_input**
-   **[Vertical layout configuration for radio buttons in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

Configurable workspaces now support a vertical layout configuration of radio buttons.

-   **[More dictionary attributes available for selected fields in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

Applicable fields used in a configurable workspace now support the following dictionary attributes:

    -   **choice**
    -   **decimal**
    -   **float**
    -   **html\_editor**
    -   **integer**
    -   **ip\_addr**
    -   **is\_searchable\_choice**
    -   **phone\_number\_e164**
    -   **readonly\_clickthrough**
    -   **ref\_ac\_columns**
    -   **translated\_html\_editor**
    -   **types**
-   **[New plugins available for the TinyMCE HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configuring-the.md-plugins-for-tinymce.md)**

The TinyMCE HTML editor now supports two new plugins in Core UI and configurable workspaces:

    -   The Image Editing \(editimage\) plugin adds a contextual editing toolbar to images in the editor.
    -   The Help plugin \(help\) enables you to check shortcuts and keyboard navigation for accessibility.
-   **[New run types available for scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_ScheduledJobs.md)**

The following run types are now available for all scheduled job types, enabling flexible scheduling:

    -   **Day and Month in Year**
    -   **Day in Week in Month in Year**
    -   **Week in Month**
The new run types are available in the following standard scheduled job types:

    -   **Scheduled Email of Report**
    -   **Scheduled Entity Generation**
    -   **Scheduled Script Execution**
To enable these new run types in other scheduled job child tables, you must configure your applicable form view to include the fields **Day**, **Month**, and **Year**. For more information, see [Enable run types for scheduled job child tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/customize-run-times-for-scheduled-jobs.md).

-   **[New advanced options available for scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_ScheduledJobs.md)**

The following new advanced options are available when configuring scheduled jobs, offering greater flexibility in job planning, execution, and recurrence:

    -   **Starting**
    -   **Ending**
    -   **Repeat every**
-   **[Export lists to Google Sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/setup-gsheet-export.md)**

Export your lists to Google Sheets directly from the Export menu.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Get type checking and validation of client-side TypeScript files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-development-react.md)**

Full-stack TypeScript applications support type checking and validation of `.ts` and `.tsx` files in the `src/client` directory when building applications.


-   **[Manage dependencies with additional parameters on the dependencies command](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-sdk-cli-commands.md)**

Control which dependencies and TypeScript definitions to download with additional parameters on the `now-sdk dependencies` command.

-   **[Use additional column types with ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/table-api-now-ts.md)**

Use the following additional types of table columns with ServiceNow Fluent APIs: Password2Column, GuidColumn, JsonColumn, NameValuePairsColumn, UrlColumn, EmailColumn, HTMLColumn, FloatColumn, MultiLineTextColumn, DurationColumn, TimeColumn, FieldListColumn, SlushBucketColumn, TemplateValueColumn, and ApprovalRulesColumn.


-   **[Download TypeScript definitions for script includes used in JavaScript modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/downloading-dependencies-now-sdk.md)**

Download TypeScript definitions for script includes imported in JavaScript modules from an instance using the `now-sdk dependencies` command.

-   **[Apply a template to an existing application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-sdk-cli-commands.md)**

Add template files and directories for development in ServiceNow Fluent using the `--template` parameter with the `now-sdk init` command in an existing application.


-   **[Automated Test Framework API supports additional test steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/atf-test-now-ts.md)**

Use the following test steps with the ServiceNow Fluent Automated Test Framework API.

    -   atf.form.addAttachmentsToForm
    -   atf.form\_SP.addAttachmentsToForm
    -   atf.server.addAttachmentsToExistingRecord
    -   atf.server.runServerSideScript
    -   atf.server.setOutputVariables
-   **[Build command doesn't package build artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-sdk-cli-commands.md)**

Use the `now-sdk pack` or `now-sdk install` commands to package build artifacts. The `now-sdk build` command compiles the source files but doesn't package the build artifacts.


</td></tr><tr><td>

Skills Foundation

</td><td>

-   **[Skills Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/skills-intelligence.md)**

Skills search is powered by AI Search capability instead of machine learning models. You can configure the skill search to be indexed based on the skill name or description or both. For Pro Plus License \(i.e. LLM Integration\) customers, AI search with RAG configuration is provided to power skill search.

Multilingual skill support is limited to the languages supported by AI Search, which is fewer than the previously supported 23 languages.

Resume parsing is done using Now Assist.

ITSM skills previously stored in the CDS plugin were moved back to the seed data plugin.


-   **[Skills Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/skills-intelligence-workspace.md)**

The application name Skills Intelligence Workspace has been changed to Skills Workspace.

Role group skill recommendations will not be readily available unless you load your own ontology data to the industry plugin.

In Skill Harmonization, duplicate skills identification relies on AI search instead of ML models, which will have some quality impact in identifying duplicates.

In Skills Import, two new integration options are added for SAP SuccessFactors and skills and user skills imported go through harmonization pipeline.


-   **[Career tab in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/manage-skills-profile.md)**

In the Career tab, the recommended skills source is now derived both from skills that are tagged to activities that employees has been pursuing and from similar user skills.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Publisher optimizations for Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/pub-opt-microsoft.md)**

The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.

-   **[Publisher optimizations for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/pub-opt-sap.md)**

The Publisher Optimizations dashboard for SAP has been updated with a report on SAP HANA Database monthly peak usage.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Components installed with Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/installed-with-FSC.md)**

The Negotiation event table label has been renamed to Sourcing event. This change affects the label only. The underlying table name, \[sn\_shop\_negotiation\_event\], remains unchanged.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Investment type and Investment class fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/planning-item-form.md)**

The **Investment type** and **Investment class** fields have been deprecated from the Project and Demand planning item tables. These fields are now created at the parent level in the Planning item \[sn\_align\_core\_planning\_item\] table.

-   **[Goal management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/managing-goals-in-alignment-planner-workspace.md)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed across the workspace. This change applies to the **Dashboards** and **Goals and targets** tabs on the Goals page, the **Goal**/**Parent goal** reference fields in all applicable tables, and all relevant dashboards.

-   **[Default related list view changes for Stories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/create-single-or-multiple-child-items-for-epic-in-eap.md)**

In the Stories list for an Epic, Feature, or Capability in the Enterprise Agile Planning workspace, the Assignment group and Sprint columns in the default related list view are replaced with the EAP team and Iteration columns.

-   **[Enhancements to tables in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/docs-for-planning-items-in-spw.md)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.

</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Streamlined user-based subscription allocation starting in Zurich Path 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/managing-user-subscriptions-v2.md)**

To simplify the Subscription Management experience, the manual allocation workflow for user-based subscriptions has been removed for administrators who have never used it. Administrators who have manually allocated user-based subscriptions before can still make manual allocations.

-   **[Assist usage excludes demo data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Demonstration instances are excluded from the total Assist usage count to improve tracking of Assist consumption.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

Now Assist usage measurement is evolving. If your instances are below Zurich Patch 6, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Hidden user-based subscription allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/subscriptions-overview-v2.md)**

To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Define network service instance details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create_application_services.md)**

**xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-network-inventory/create_business_applications.md)**

**xNF** is renamed to **Network Function**.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Telecom Discovery via Nokia Altiplano](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-service-ops/service-graph-connector-for-nokia-altiplano.md)**

Nokia Altiplano SGC enables you to do the following:

    -   Discover logical inventory for Nokia Altiplano such as logical ports, LAGs, and logical connections.
    -   Enable customers to manage both physical infrastructure and logical network relationships on the ServiceNow AI Platform.
    -   Store logical elements in the CMDB, improving visibility and traceability across the network.
    -   Use the generic Extract, Transform, Load \(ETL\) framework provided by ServiceNow to integrate with Nokia Altiplano, significantly reducing development effort.
-   **[Discrepancy identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-service-ops/discrepancy-identification-types-of-discrepancies.md)**

Use the enhanced audit and reconciliation logic to do the following:

    -   Detect mismatches in logical elements such as logical ports, LAGs, and connections.
    -   Filter audit results by IP range, device type, or vendor to focus on relevant subsets of data.
    -   Enhance audit performance, usability, and customer satisfaction by reducing unnecessary processing.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Risk areas extended to internal assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-sae-q-template.md)**

Starting with version 21.1.x, if you have the third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_admin\] role, you can now configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace. Risk scores can be aggregated at the engagement level using customizable methods such as max, min, or average, and mapped to risk ratings based on business rules. Risk managers can override system-generated ratings with required justification, enabling expert judgment and helping ensure transparency in risk decisions.

-   **[Smart Assessment Engine advanced plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-migrate-asmnt-sae.md)**

Starting with version 21.1.x, the following Smart Assessment Engine advanced plugins are automatically installed: Post Assessment Actions for Smart Assessments \[com.sn\_smart\_imp\_auto and com.sn\_impact\_fwk\] and Advanced Response Automation for Smart assessments \[sn\_smart\_resp\_auto\]. The Post Assessment Actions for Smart Assessments plugin lets Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] automate follow-up tasks, like notifications or workflow launches, after an assessment is completed. The Advanced Response Automation for Smart Assessments plugin automatically fills in assessment responses based on prior data or logic, streamlining and standardizing the assessment process.

-   **Feature-specific administrator role enhancements**

Starting with version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

    -   Assign sn\_vdr\_risk\_asmt.vendor\_risk\_admin to users who need to configure and manage vendor risk features.
    -   Assign sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer to users who perform assessments, manage dashboards, and require operational access.
    -   Assign sn\_vdr\_risk\_asmt.external\_assessment\_responder to users who need access to the third-party portal and to complete assessments.

**Note:** Administrator privileges no longer grant access to TPRM features. Users must be assigned an appropriate feature-specific role to access relevant functionality.

-   **Read-only field enhancements**

Starting with version 21.1.x, the following Third-party Risk Management plugins have security enhancements for read-only fields in this release:

    -   Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\]
    -   Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\]
    -   GRC: Vendor Portal \[com.sn\_grc\_vendor\_portal\]
    -   GRC: Profiles \[com.sn\_grc\]
    -   GRC: Compliance Assessment \[com.sn\_comp\_asmt\]
    -   GRC: SIG Questionnaire Integration \[com.sn\_sig\_asmt\]
    -   GRC: Performance Analytics Premium Integration \[com.sn\_grc\_pa\]
    -   Vendor Risk Management integration with EcoVadis \[com.sn\_app\_grc\_ecovadis\]
    -   ITAM applications \[com.snc.vendor\_core\]
-   **[Fourth-party assessment support in SAE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-monitor-fourth-parties.md)**

Starting with version 21.1.x, Fourth-party assessments are now supported after you enable the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   ****

Aggregate and analyze the data from internal systems through internal intelligence included in the Investigation Canvas module to help you identify potential threats more effectively.


-   **[Import Intelligence in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/importing-threat-intelligence.md)**

Enhanced the Import Intelligence functionality to support direct import of allow list observables.

-   **[Working with Investigation Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/tisc-investigation-canvases.md)**

The Investigation Canvas feature has been extended to include customized nodes, node relationships, and node legends, as well as the grouping and ungrouping of nodes.

-   **[Investigation canvas and MITRE ATT&amp;CK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/investigation-and-mitre.md)**

Navigate and use the MITRE-ATT&amp;CK model within the Investigation Canvas more effectively by taking advantage of enhanced filtering options.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Add events to track components with unsaved changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/dirty-state-event.md)**

Use an event to quickly identify modified components.

-   **[Configure alerts to auto-dismiss](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/uib-configure-alerts.md)**

Enable alerts to auto-dismiss across an experience by configuring all of them in the experience settings or individually through an event.

-   **Use pages across experiences**

Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.

-   **[Use the floating Now Assist panel to streamline your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/uib-now-assist-panel.md)**

As of UI Builder version 28.2, the fixed Now Assist panel has been replaced with a drag-enabled floating panel improving layout flexibility and workflow visibility.

-   **[Specify your page type in the Create a page wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-page.md)**

As of UI Builder version 28.2, the Create a page wizard now includes a page**Type** dropdown field. This new field helps you to later identify and filter important pages within the Experience view list, especially helpful in large experiences with many pages.

-   **[Explore the newly enhanced Experience view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/nav-uib.md)**

As of UI Builder version 28.2, the Experience view has improved usability in the following ways:

    -   Pages and their variants appear collapsed by default for a cleaner, more focused view.
    -   Locate pages and variants with ease utilizing the search field.
    -   Search by name, URL, URL type, or variant, and toggle between filters for a cleaner, more intuitive page list.
    -   Pagination is automatically enabled when 10 or more pages are present.

</td></tr><tr><td>

Upgrade Console

</td><td>

-   **[Updated access to Guided upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/um-guided-tour-implement.md)**

Apart from the **Guided upgrade** tab option, you can also access Guided upgrade by selecting **Resume upgrade** if there is an ongoing upgrade in the instance.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[Table bot response control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/table-bot-response.md)**

Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **[Test assistant options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/test-llm-topics.md)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/visa-spoke.md#section_gsl_nw5_vyb)**

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

Vulnerability Response

</td><td>

-   **[Granular VIT creation for Microsoft TVM recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-configure-vi-key.md)**

You can now configure recommendation as a vulnerability item \(VIT\) key for Microsoft Threat &amp; Vulnerability Management \(TVM\). This enhancement enables each recommendation to generate a separate vulnerable item, offering more granular control for tracking, assigning, and managing remediation efforts, especially when different recommendations require actions from different teams.

-   **[Improved state management for remediation tasks and vulnerable items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-rt-states.md)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.

-   **[Ability to manually cancel Exposure Assessment background jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-ws-exposure-assessment.md)**

Vulnerability Admins and Event Managers can now cancel Exposure Assessment background jobs that were triggered with incorrect parameters or are taking longer than expected. This enhancement reduces downtime by removing the need to wait for the job to complete. After the job is cancelled, the substate is immediately set to User cancelled, and the state updates to Complete after the job is fully terminated; giving you better control and flexibility.

-   **[Configure maximum rows in related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-max-rows-rel-list.md)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Qualys Integration – Detection Splitting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/split-qualys-detections.md)**

Use the Qualys Host Detection Integration to create a separate VIT for each vulnerability instance based on proof. This improves accuracy in vulnerability tracking and supports clearer team ownership during remediation.

-   **[Activate the Qualys QVS score integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/optional-modifications.md)**

Add Qualys-specific risk context to CVEs by importing QVS scores, helping you make more informed prioritization decisions.


</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   **[SAP ECC primary connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/sap-ecc-primary-wdf.md)**

The SAP ECC connector is now certified as a primary connector.

-   **[SAP S/4HANA primary connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/sap-s4hana-primary-wdf.md)**

The SAP S/4HANA connector is now certified as a primary connector.

-   **[Primary connectors in preview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/primary-connectors-wdf.md)**

Primary connectors that are still being enhanced to include all planned functionality are now identified as in preview. These connectors are fully supported by ServiceNow®.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   **Additional system property to specify how many records are retrieved**

The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Zero Copy Connector for ERP Enterprise Data Foundation data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-enterprise-data-foundation-content-pack.md)**

Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Quote to Cash data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-sales-order-content-pack.md)**

Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Source to Settle data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-source-to-settle-data-product.md)**

Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/release-notes-summaries.md)

