---
title: Changes to Zurich features and products
description: Cumulative release notes summary on changes to Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 146
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

-   **[Security &amp; privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   The Autonomous vs. supervised AI tools chart has been removed.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes in Zurich Patch 4](../quality/zurich-patch-4.md)**
    -   The AI asset inventory plugin structure has been updated.
    -   Product owner view: Added a role called AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\], which enables the Product Owner view experience with a personalized home page and enhanced visibility into AI assets to simplify task management.
    -   AI discovery: The Innovation lab store application \(AWS AI discovery plugin\) is decommissioned. Uninstall the AWS AI discovery plugin prior to installing the AI discovery plugin \(sn\_ai\_disc\).
    -   AI cases management has moved under the **AI cases** tab on the AI Control Tower home page.

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[AI risk and compliance home page](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The **Risk and compliance** tab now features dedicated Risk overview and Compliance overview sections that enable you to continuously monitor the risk and compliance posture of your AI assets.

The Risk overview section is a filtered view of your AI assets that are based on inherent and residual risk levels so that you can make informed risk evaluations. The Compliance overview section displays the regulatory risk classification of AI systems, models, and datasets through donut charts. Additionally, you can see the compliance status of your AI assets in relation to applicable authority documents and internal policies.

-   **[Worknotes and comments in AI system records](https://www.servicenow.com/docs/access?context=ai-system-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The AI system record now supports worknotes and comments. You can now document decisions, share updates, and provide context throughout the AI risk and compliance life-cycle. Worknotes and comments help improve the communication among stakeholders and ensure a comprehensive audit trail.

-   **Feature-specific administrator role enhancements**

Starting with version 21.1.1, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


-   **[Consumer-grade search experience for search portals](https://www.servicenow.com/docs/access?context=viewing-search-results-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://www.servicenow.com/docs/access?context=using-ais-next-experience-app&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://www.servicenow.com/docs/access?context=create-facet-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://www.servicenow.com/docs/access?context=grouping-attachment-srch-results-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


</td></tr><tr><td>

API

</td><td>

<table id="table_x1g_1mc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideSysAttachment - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSysAttachmentScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngine - Scoped](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[ProducerV2 - Scoped](https://www.servicenow.com/docs/access?context=ProducerV2ScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

send\(\) - Added a return value and error handling.

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

createInstance\(\) now supports the **allowedContextTypes** parameter, enabling partial synchronization of updates or deletions for selected Related Parties back to the originating Opportunity. Previously, partial synchronization behavior was limited to quote line items only.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

1.6

</td><td>

2025-12

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

To allow more complex business needs, getPrimitivesEPService\(\) supports the new **context.entityConfigId** parameter, which invokes createInstance\(\) script without any defined mapping using only the entity's configuration ID.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Remove support for groups in Dynamic Schema. -   getGroupName\(\)
-   getName\(\)
-   getPath\(\)
-   getType\(\)
-   isTransient\(\)

Remove getSysId\(\).

Remove GlideTransientDynamicAttribute API documentation because GlideDynamicAttribute and GlideTransientDynamicAttribute APIs provide the same solution.

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[GlideSysAttachment - Global](https://www.servicenow.com/docs/access?context=GlideSysAttachmentGlobalAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngineScriptableApi - Global](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

When submitting a change payload with a new or updated service location \(via **productOrderItem.product.place.id**\), the request is now processed as a move order. This means that the product order remains the same but the service is fulfilled in the new designated location.-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&section=tmf_prod_order-PATCH-ord-productOrder-id&ft:locale=en-US)
-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&section=tmf_prod_order-PATCH-productorder-id&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&section=tmf_prod_order-POST-ord-productOrder&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&section=tmf_prod_order-POST-productOrder&ft:locale=en-US)

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2025-12

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Trouble Ticket Open API](https://www.servicenow.com/docs/access?context=trouble-ticket-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/threat\_intel\_data/observables now supports filtering observables on tags and taxonomies.

</td></tr><tr><td>

Accounts Payable Invoice Processing

</td><td>

v9.5.17

</td><td>

2025-08

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

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

[Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

New options for the **action** request body parameter with corresponding examples.POST /sn\_va\_as\_service/bot/integration

</td></tr></tbody>
</table>

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Invoice exceptions](https://www.servicenow.com/docs/access?context=work-with-invoice-exceptions&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Insufficient goods receipt exception has been enhanced to validate line-level quantities accurately when multiple invoices are submitted against a single purchase order even if a sufficient goods receipt exist.

The Insufficient Funds \(Line Amount\) functionality has been enhanced to perform validation of available funds at the invoice line level, matching each invoice line against its respective purchase order line when multiple invoices are generated for the same purchase order line.

The Insufficient Funds \(Header Amount\) logic has been enhanced to validate available funds at the invoice header level against the corresponding purchase order when multiple invoices are created for the same purchase order.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The performance metrics, trends, and charts for this dashboard have been refreshed to offer a cleaner visual experience.


-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The **Date range** interactive filter now enables you to access data from the last 180 days, rather than the last 90 days.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Thin compose modeless dialogs](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US#section_nws_1rs_rfc)**

Enable agents to initiate a comment, work note, or email in the activity stream and then open the text in a modeless dialog. This feature is available on the following record pages:

    -   Front-line case page
    -   CSM default record page
    -   CSM Interaction record page
    -   CSM voice interaction record page
    -   CSM centered chat interaction record page
    -   Email interaction record page
-   **Activity Stream enhancements**
    -   Activity Stream layout now automatically adjusts to your device \(laptop, tablet, or mobile\). Hidden content is indicated by \(...\) for better readability.
-   **[Lookup component on CSM Configurable Workspace record pages](https://www.servicenow.com/docs/access?context=csm-record-page-lookup-component&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the Lookup component to look up and link a contact and then verify the contact. The Lookup component replaces the Lookup and Verify component on the CSM Configurable Workspace record pages.

-   **Hide inbox after item selection**

The Inbox panel collapses after selecting an inbox item, enabling agents to see more of the screen and focus on the interaction.

-   **Multi-form controller support**

Supports having two forms on a record page.

-   **Real-time notification count updates**

Updated the bell icon behavior so the notification count accurately reflects the number of unique, unread notifications in real time, eliminating duplicate increments.

-   **[Customer History enhancements](https://www.servicenow.com/docs/access?context=customer-history-component-features&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the following enhancements to control grouping, appearance, and refresh behavior in customer history:

    -   Enable time grouping by month or quarter: A new property enables selection of time grouping as monthly or quarterly \(Q1-Q4\) in date filters.
    -   Customize feed appearance: Admins can configure feed icons along with their background colors using a property that offers predefined color options.
    -   Display activities by updated date: A new property enables feeds to surface activities based on the last updated timestamp in Customer History.
    -   Dynamic refresh updates: Customer History feeds now refresh automatically, but only for records in the Customer History activities table and within the current context \(for example, Contact\). Other tables and parent records are not included.
    -   Introduced a new search icon that lets agents show or hide the search bar with a click.
-   **[Improve discoverability of Recommended Actions](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

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
-   **[Default recommendations for Pro customers](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Recommendations are now delivered by default for Pro customers when either the Task Intelligence for CSM or the Now Assist for CSM plugin is installed. Agents can view contextual recommendations under the **Suggested Actions** tab, such as similar cases and open incidents, when the case meets the predefined criteria. Agents can link or copy resolutions directly into the current case.

-   **[Resurface special handling notes](https://www.servicenow.com/docs/access?context=c_OnScreenAlerts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Display the special handling notes at any time by selecting  Special handling notes  from the More actions menu on the case record action bar. This action is now available on records from the following tables:

    -   Account
    -   Asset
    -   Contact
    -   Incident
    -   Product Model
    -   Work Order Task
This applies only to records where special handling notes are configured.

-   **[Information session tab enhancements](https://www.servicenow.com/docs/access?context=csm-workspace-chat-session-tabs-configure&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the following changes to enforce permissions and improve usability of the **Session** tab:

    -   Restrict access to unauthorized users with error messages and validate role-based permissions.
    -   Auto-save admin updates to timer and color changes in real time.
    -   Display workspace settings only after the Session tab is enabled.
-   **[Configure Alert Dismissal settings at experience and alert level](https://www.servicenow.com/docs/access?context=auto-dismiss-alerts-in-csm-configurable-workspace&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the following settings to control alert dismissal:

    -   Set alerts to auto-dismiss or require manual dismissal.
    -   Configure alert behavior globally or according to alert.
    -   Reduce alert overload while supporting accessibility standards, which helps agents focus on critical alerts.
-   **[ServiceNow Link Manager is available on the Google Chrome, Microsoft Edge, and Mozilla Firefox plugin store](https://www.servicenow.com/docs/access?context=csm-workspace-snow-link-manager&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Streamline tab management and reduce browser clutter with ServiceNow Link Manager:

    -   Automatically consolidates new ServiceNow related tabs into an existing open ServiceNow tab.
    -   Provides cross-platform support.
    -   Enables agents to share record links, such as cases, through platforms like Gmail, Microsoft Teams, Microsoft Outlook, and other web tools integrated with ServiceNow. These links open using ServiceNow Link Manager, ensuring the record loads in the correct workspace and context.
    -   Provides a user-friendly interface that is easy to enable and turn off directly from the extension settings in the respective browser.
-   **[Follow records to receive notifications](https://www.servicenow.com/docs/access?context=csm-default-record-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US#section_follow_action)**

Select the **Follow** action to receive notifications when comments or work notes are added to a record. The Follow action is available in the More actions menu on the [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).


</td></tr><tr><td>

App Engine Studio

</td><td>

-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=aes-personas-roles&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Separate App Engine Management Center release notes](../now-platform-app-engine/aemc-rn.md)**

The App Engine Management Center \(AEMC\) release notes now appear separately from the App Engine Studio release notes because you can use AEMC to manage app development for apps built in App Engine Studio, Creator Studio, and ServiceNow Studio. For information about AEMC, see [App Engine Management Center release notes](../now-platform-app-engine/aemc-rn.md).


</td></tr><tr><td>

Application Manager

</td><td>

-   **[Unlicensed application information](https://www.servicenow.com/docs/access?context=available-for-you-app-mgr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

In addition to details about applications that are already licensed, the "Available for you" tab of the Application Manager now includes information about applications that haven't been procured from the ServiceNow Store yet.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=avm-configuring&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Enhanced SSO login and logout experience](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://www.servicenow.com/docs/access?context=mfa-with-fido&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://www.servicenow.com/docs/access?context=oauth-inbound-and-outbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Configure OAuth integration that includes the following enhancements:

    -   You can provide a maximum client secret length up to 4096 characters to meet security requirements of the third-party systems.
    -   You can provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
    -   You can request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\). It also supports RS256, RS384, RS512, HS256, HS384, and HS512.
    -   You can customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

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
-   **[Task plan template configurations](https://www.servicenow.com/docs/access?context=task_plan_template_configurations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Admins can create configurations for task plan templates that pre-fill information when creating a new task plan template.


-   **[Filtering service definitions](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable agents to filter the service definitions that are shown on the service selector in the following ways:

    -   By user, role, group, or agent
    -   By entity critera such as location, customer level, or related entities
-   **[Case lines for Case Management - Add multiple entitlements to case lines](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

View the available entitlements on a case line and associate the multiple entitlements to that case line. Available entitlements are associated with the contracts and entitlements that are purchased by the customer.

-   **[Targeted Communications](https://www.servicenow.com/docs/access?context=targeted-comm-publication-workflows&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and [Case Digests](https://www.servicenow.com/docs/access?context=customer-service-case-digests&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US#section_ast_r2k_qfc) workflows**

Legacy workflows for the Targeted Communications \(com.sn\_publications\) and Case Digests \(com.sn\_csm\_case\_digest\) applications have been migrated to low-code flows in Workflow Studio. The functionality of the flows remains the same.

-   **[Classifying sensitive data](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Fields in the Customer Service Management and Targeted Communications tables are mapped to the Data Privacy data classes. For more information, see the [Data privacy overview](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **Deny-Unless ACLs implemented on CSM tables**

Deny-Unless access control lists \(ACLs\) were implemented on CSM tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only authenticated users can perform read, write, delete, or create actions on these tables. For more information about Deny-Unless ACLs, see the [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **[Customer Service Case Types moved from family to store release](https://www.servicenow.com/docs/access?context=customer-service-case-types&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Starting with the Zurich release, the Customer Service Case Types application \(sn\_csm\_case\_types\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Service Case Types store app.


</td></tr><tr><td>

Change Management

</td><td>

-   **[Propose a standard change template in Service Operations Workspace](https://www.servicenow.com/docs/access?context=propose-standard-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As a user with the itil role, you can create a standard change template proposal in Service Operations Workspace.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://www.servicenow.com/docs/access?context=config-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[My Work enhancements](https://www.servicenow.com/docs/access?context=my-work-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Track all your work from one place using the enhanced My Work in CWM. My Work now supports all ServiceNow task records-such as incidents, changes, and requests-whether they originate in CWM or outside, giving you a unified view of everything assigned to you. This helps you stay on top of overdue or open tasks and improves on-time delivery.

Additionally, the Item type filter has been refined to show all CWM tasks \(including custom ones\) grouped under a single category, instead of listing every CWM task type individually. You’ll also only see task types in the filter that you’re actually assigned to, reducing clutter and making it easier to filter what matters.

-   **[Enhancements to tables in Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.
    -   Select multiple cells of a table using the mouse device or by pressing **Shift+ one of the arrow keys** on the keyboard.
    -   Delete content from multiple cells using the **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy content from one cell and paste it to multiple cells.
        -   Copy content from n number of cells and paste it to another set of n number of cells.
        -   Copy content from multiple cells and paste it as a new table in an empty block on the page.
-   **[Enhancements to CWM Board templates](https://www.servicenow.com/docs/access?context=templates-in-cwm-for-spaces-boards-and-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Save template: While saving a Board as a template, choose between saving the current view or all shared views. You can see the number of Board views and custom task types that are included in this template.

These details are displayed in the Template Center, where you can select a template that best meets your team's needs.

    -   Apply template: While applying a Board template, you can see the number of Board views and custom task types that you get if you apply this template. The Board views drop-down list lets you switch between views and provides information on the type of views that are enabled in this template.

Only those custom columns that are part of these views are brought over when you apply this template.

-   **[Collaborating with Spaces in CWM](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

When a user is added to the **Assigned to** field of a CWM task but doesn't yet have access to the Space, the email notification requesting access is sent only to the Space owners. This way, there's less email clutter for all the Space users because notifications are sent to only those users who need to know this information.

-   **[New columns for CWM tasks](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Every task within a CWM Board has new columns called Sprint and Story points. You can use these columns if you choose to plan any task into Sprints. These columns are available on every type of work item, including the items that are brought into the Board through Connected work.

-   **[Changes within CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Open the keyboard shortcut panel:
        -   macOS: Cmd + Option + K
        -   Windows OS: Ctrl + Alt + K
    -   Images can be resized after inserting them within a table cell.
    -   The page name can be updated by editing the name and clicking anywhere on the Doc.
    -   Moving content blocks to within a numbered list or deleting a list item from a list automatically adjusts the list numbering.

</td></tr><tr><td>

Common Core

</td><td>

-   **[States in the entity based record access update utility](https://www.servicenow.com/docs/access?context=eba-configuration-states&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

A new Preview state has been added to the record access update utility life cycle. You can now review the estimated number of impacted records before you apply the restrictions. This step helps you to validate the selected scope, assess potential impacts, and make adjustments, if needed. It also adds an extra layer of control and reduces the risk of unintended access changes.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **[Browser warning for unsaved changes](https://www.servicenow.com/docs/access?context=config-browser-warning-unsaved-changes&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Configure a browser warning to alert you of unsaved changes when you navigate away from a page using the back or forward buttons.

-   **[Record List component bundle enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20list/overview)**

Configure these enhancements to the Record List component bundle in UI Builder:

    -   Select **Related** list as a list type option.
    -   Switch between the standard view and gallery list, which displays list items as cards.
-   **[Export lists to Google Sheets](https://www.servicenow.com/docs/access?context=exporting-lists-google-spreadsheets&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Export your lists to Google Sheets directly from the Export menu.

-   **[Live updates for lists](https://www.servicenow.com/docs/access?context=live-list-updates-configurable-workspace&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Configure live updates at the list page level without affecting other lists in your Configurable Workspace.

-   **[AI filter assist](https://www.servicenow.com/docs/access?context=use-ai-filter-assist&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

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
-   **[Personalize Form menu](https://www.servicenow.com/docs/access?context=hide-personalize-form-menu&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Customize which fields display on a form with the Personalize Form menu \(![image.icon-personalize-form]\) in the form header. Use system properties to hide the Personalize Form menu or change the roles with access to the menu.

-   **[Format string fields with guidance text and inline validation](https://www.servicenow.com/docs/access?context=format-regex-pattern-string-fields&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Set up guidance text to display in string fields with format requirements such as account ID, SSN, or SIN. Use regular expression inline validation to display an error message if input values are incorrect.

-   **[Advanced view rules configuration](https://www.servicenow.com/docs/access?context=configure-advanced-view-rules-forms&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Use client scripts to set up view rules configurations.

-   **[Activity Stream Compose component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-activity-stream-compose-connected/uib-setup)**

Configure these enhancements to the Activity Stream Compose component in UI Builder:

    -   Hide the rich text editor toggle for your workspace without affecting other experiences.
    -   Rename and reorder Emails, Work notes, and Comments tabs.
    -   Annotate new activities to make it easier for you to find unread emails and messages.
-   **[@mentions for the email composer](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/shared-components/now-email-client-composer-connected/overview)**

Configure @mentions in UI Builder for the Email composer and Email composer \(mini\) components, enabling you to add an email recipient by using an @mention in the email body.

-   **[Digital signature and encryption in the email composer](https://www.servicenow.com/docs/access?context=config-email-digital-signature-encryption&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Send emails with a digital signature that verifies you as an authentic sender and an email encryption that certifies authentic recipients.

-   **[Custom attachment layout](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-record-common-attachments-connected/uib-setup)**

Configure a custom layout mode for the Attachments component in UI Builder. Customize the maximum file size, file types, multiple file uploads, and preview modal.

-   **[Adding the Now Assist icon to action buttons](https://www.servicenow.com/docs/access?context=create-da-buttons-now-assist-icon&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Use declarative actions to create buttons with the Now Assist \(![](../../common/image/icon-ai-sparkle.png)\) icon and hover animation.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **Optimized Tenable.io Compliance Results ingestion**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is deprecated and replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Configure Tenable test result granularity](https://www.servicenow.com/docs/access?context=cc-tenable-tr-granularity&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v15.6.1, you can configure the granularity of Tenable Configuration Test Results \(CTRs\) to split results into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure Qualys Test Result Granularity](https://www.servicenow.com/docs/access?context=cc-qualys-tr-granularity&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v15.4.3, you can configure the granularity of Qualys Configuration Test Results \(CTR\) in configuration compliance and split CTRs into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=vr-max-rows-rel-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**
    -   On the Published policy tile on the Data Manager policies page, the policies list view now shows the scheduled job that is associated with the policy and the user that the policy runs as.

For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   Instead of the system automatically setting the **run as** attribute of the scheduled certification and attestation jobs to be the user that authored the policy, you can now set a specific user that adheres to the policies and regulations in the organization. Configure the default values for the run as user and user accounts available for run as assignees for auditing purposes when it’s important to know who initiated the changes.

For more information, see [Components related to CMDB Data Manager](https://www.servicenow.com/docs/access?context=components-cmdb-data-manager&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   For certification and attestation policy tasks, choose how to assign tasks in cases where a specified task assignment field is empty for a target CI. Specify a user or a user group to assign such tasks to, or create the tasks without assigning them. An administrator can later review and assign those tasks.

For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   View the closed tasks in the My Work view in CMDB Workspace. Select the Closed card in the Task status tile to review the \(in read-only mode\) details for tasks that are in the Closed Complete, Closed Canceled, Closed Incomplete, or Rejected state.

For more information, see [My Work view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-govern-view&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   New CIs in the Create CI experience no longer have their **Operational status** attribute set. The new **CI Operational state** attribute appears on the Additional attributes page of the Create CI experience. Setting it to any value is optional.

For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   The itil user role now contains the sn\_cmdb\_user user role and no longer contains the sn\_cmdb\_editor user role. As a result, the following functions that were accessible to itil users now require the sn\_cmdb\_editor user role:
        -   Create and delete the operations that are related to CMDB 360 queries.
        -   Access the CMDB Retirement Definitions module by navigating to **All** &gt; **Configuration** &gt; **CMDB Retirement Definitions**.
        -   Access the Create CI quick link on the Home view of CMDB Workspace.
-   **[Containment in the itil user role](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

In zBooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

-   **[Constraints when deleting a CMDB Data Manager retirement definition](https://www.servicenow.com/docs/access?context=data-manager-manage-ret-def-wrkspc&version=zurich&pubname=zurich-servicenow-platform&section=data-manager-delete-ret-def-wrkspc&ft:locale=en-US)**

The same constraints that exist when deleting a retirement definition in CMDB Workspace now apply when directly accessing the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table:

    -   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
    -   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.
-   **[Prioritize using IRE identification rules for uniquely identifying CIs](https://www.servicenow.com/docs/access?context=ire&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Configure the system to prioritize the use of IRE identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** fields. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to control this behavior, see [Properties](https://www.servicenow.com/docs/access?context=properties-id-reconciliation&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   **[Run a query in an enhanced execution mode](https://www.servicenow.com/docs/access?context=config-query-builder-engine-mode&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Set the execution mode for a saved CMDB Query Builder query to run using an enhanced query execution engine, which is designed for improved performance and scalability.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=vr-max-rows-rel-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[New Authorization Documents tab for ATO reports](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Access all Authority to Operate \(ATO\) artifacts reports from the new **Authorization Documents** tab available in the Authorization Package.


-   **[New CAM System Properties page for administrators](https://www.servicenow.com/docs/access?context=cam-components-installed&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Access the new CAM **System Properties** page to enable administrators to configure various system properties.

-   **[Track package progress with the Ageing of Packages widget](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

View the duration that a package stayed in each step, like Prepare, Categorize, Select, Implement, Assess, Authorize, and Monitor, using the Ageing of Packages widget.

-   **[Set Next Engagement Date for Automated Audit Generation](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Enter the **Next engagement date** to automatically generate the audit engagement on the specified date.


</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Send contracts for signature using Adobe Sign without signing in](https://www.servicenow.com/docs/access?context=cncore-nss-review-request&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Send contracts for signature in Adobe Sign without requiring users to sign in to the e-signature portal. Any modifications to the signatory details and contract documents are restricted in the Adobe Sign portal and must be completed in Contract Management Pro before initiating the signature process.

-   **[Compare contract revisions in Contract Management Pro](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Compare contract revisions of a contract document stored in external storage.

-   **[Validations for content control placement in the Microsoft Word add‑in](https://www.servicenow.com/docs/access?context=cncore-addin-add-clauses&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

See when a clause, table, or signature block is incorrectly tagged while configuring a contract template through validation messages displayed in the Microsoft Word add-in.

-   **[Improved Microsoft Word document processing](https://www.servicenow.com/docs/access?context=cncore-set-ext-app-config&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Contract Management Pro now supports processing of Microsoft Word documents larger than 10 MB. This enhancement applies to all document operations such as contract revision generation, document synchronization, and document comparison.

-   **[Select contract type while initiating a third-party contract](https://www.servicenow.com/docs/access?context=cncore-initiate-non-ss-cnt&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Specify whether a contract request is for a single contract or multiple contracts. For single contracts, you can select the type of contract document.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://www.servicenow.com/docs/access?context=snlc-submit-request-tpc&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Automatically classify a contract request as single contract type or multiple contracts type based on single or multiple contracts when creating a third-party contract review request from Employee Portal. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://www.servicenow.com/docs/access?context=cncore-add-clauses-doc-tmplt&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Define clause conditions on fields and variables of a table that isn’t directly linked to the contract template table. The condition determines when the clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://www.servicenow.com/docs/access?context=cncore-append-data-table&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Insert additional data from the related table fields into the dynamic tables of a contract using scripts. Display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://www.servicenow.com/docs/access?context=cncore-create-ct-word-addin&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

-   **[Configure dynamic tables for contract template](https://www.servicenow.com/docs/access?context=cncore-addin-table&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Set up contract templates on the Contract Request \[sn\_cm\_core\_contract\_request\] table to reuse the template across business units. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

Additionally, the **Table** field has been renamed **Lookup table**. You can select the table from the data that is populated into the contract document.

If the template isn’t based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Copy fields from parent request to contract request](https://www.servicenow.com/docs/access?context=cncore-copy-fld-frm-parent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Automatically copy the required fields from the originating business unit record to the contract request when it’s initiated.

-   **[Signature workflow for a contract request](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Wet signature requests are sent one signatory at a time, starting with the first signatory in order, rather than to all signatories at the same time. Signatories can be changed even after the signing process has been initiated. When a signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Modify signatories](https://www.servicenow.com/docs/access?context=cncore-pause-signature&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Resend signature request](https://www.servicenow.com/docs/access?context=cncore-resend-sign-req&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enable contract fulfillers to manually trigger a signature request when needed instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configuring signatories in Contract template using Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cncore-config-sign-addin&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\) instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Deleting questions from unpublished forms removes the record](https://www.servicenow.com/docs/access?context=creator-studio-delete-forms-questions&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Enhancements to the declarative responsibility framework](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Introduced several key improvements to enhance the flexibility and usability of the declarative responsibility framework:

    -   Enabled responsibility access configurations to support more granular access control.
    -   Updated the data model by adding new fields and renaming select field labels for improved clarity.
    -   Refreshed associated forms and lists to reflect the latest framework updates.
-   **[Updated account manager responsibility access configuration](https://www.servicenow.com/docs/access?context=list-of-reponsibilities-provided-with-base-system&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enhanced access configurations for account manager responsibilities by creating a unified entity that defines access based on record and role for more consistent and streamlined access control.

-   **[Managing account addresses](https://www.servicenow.com/docs/access?context=associate-address-account&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Manage account addresses by associating locations with accounts where the Update access is granted to confirm tracking of address information and support account management.

-   **[Updating location records associated with account](https://www.servicenow.com/docs/access?context=delete-address-location-form&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Restricts users from updating a shared location record unless they have the Update access to all associated accounts, confirming location details can only be modified with the necessary permissions across every linked account.

-   **[Delta price enhancements](https://www.servicenow.com/docs/access?context=sold-product-form&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

The following are enhancements added in Delta pricing:

    -   Added pricing fields that reference sales agreements and captures base prices on sold products to verify consistent pricing during modifications, such as quantity changes or attribute updates. New fields are added to enhance the traceability for subscription-based products.
    -   Added columns to the Sold Product base table. Use the Split from and Split from root to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.
-   **[Install base data model enhancements](https://www.servicenow.com/docs/access?context=create-install-base-item&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Improve traceability and product life cycle management with the **Serial Number** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Access control improvements](https://www.servicenow.com/docs/access?context=sold-product-form&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Provide hierarchical access to Install Base items for location managers and staff to manage assets sold by or associated with their service organizations.

-   **[Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Gain precision in sales entity setup with three new columns in the Lead to Cash Entity Definition table: Filter Conditions, Enable Post Processing, and Post Processing Script. These columns enable targeted data filtering and post-processing logic execution.

-   **[Explore partial sync](https://www.servicenow.com/docs/access?context=about-partial-sync&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Partial sync processes the data sections you specify instead of the entire structure, significantly improving performance and reducing resource consumption.

The partial sync enhancement includes improved error handling that provides clear, actionable error messages when mandatory fields are missing from synchronization requests.

-   **[Setting up products and available services at a business location](https://www.servicenow.com/docs/access?context=products-services-at-bus-loc&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)Support for service-related capabilities in business locations**

Enable service-related capabilities for business locations by activating the optional Customer Service Case Types \(sn\_csm\_case\_types\) plugin.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[Full scan support added](https://www.servicenow.com/docs/access?context=configure-data-discovery-jobs&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Data Discovery jobs support full type scans, which scan for sensitive data patterns in all the records. You can also use an incremental scan, which acts as a delta scan from the point of the last full scan.

-   **[XLS and CSV support added](https://www.servicenow.com/docs/access?context=data-discovery-attachment-scanning&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Data Discovery attachment scan type jobs now support XLS and CSV files. Attachment scans are incremental scans by default.

-   **[Text to Regex from a LLM](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Create a regex data pattern with the help of Now Assist, which supports all third-party LLMs approved by ServiceNow.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Support for MID Server cluster](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://www.servicenow.com/docs/access?context=sc-github&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://www.servicenow.com/docs/access?context=devops-reference-error-messages&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://www.servicenow.com/docs/access?context=installed-with-dev-ops&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.
-   **[Prod deploy commit logic for other step types](https://www.servicenow.com/docs/access?context=dev-ops-commits-release&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Update the **sn\_devops.commit\_rel\_change\_step\_type** property to have other step types, like Test or Deploy, use the same commit logic as Prod Deploy.

-   **[Override start and end time of a change request](https://www.servicenow.com/docs/access?context=dev-ops-config-change-details&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Set the  **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time ** and  **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time ** properties as false to consider the change request start and end time instead of the pipeline’s when the  autoCloseChange  parameter is enabled in a pipeline.

-   **[Node version of DevOps extension](https://www.servicenow.com/docs/access?context=config-dev-ops-extensions-azure&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The node version of the ServiceNow DevOps  extension has been upgraded to version 20.x in Azure DevOps.

-   **[Enhanced pipeline governance in GitLab](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View change request details like status, sys\_id, priority in the GitLab console when a change request is created in GitLab using Docker image.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
    -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in  GitHub,  GitLab,  Azure DevOps, and  Jenkins using the DevOps webhook configuration analysis health check.
    -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
    -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
    -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting  **View all findings ** in the  Health scan findings  widget. 
-   **[Enhanced JFrog integration with DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Gather JFrog evidence seamlessly and create change records automatically using the improved JFrog integration with DevOps Change Velocity.

-   **[Bearer authentication in JFrog](https://www.servicenow.com/docs/access?context=devops-jfrog-connect-workspace&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Connect to JFrog using the secure bearer token authentication to comply with JFrog’s updated security policies.

-   **[HTTP proxy for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Connect to DevOps Change Velocity through HTTP proxy settings using environment variables in your Docker deployment for instances that run a proxy server.

-   **[Health scan enhancements](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   Identify any callback processing issues in your instance.
    -   Identify any access control rule \(ACL\) that is incorrectly associated with a role in your instance.
    -   Verify whether all DevOps tables are present in your instance and confirm whether all metadata in sys\_\* tables is present.
    -   Verify whether all DevOps roles in your instance contain all expected roles, including inherited roles.
-   **[Auto close without Change Management - State Model \[Legacy\] plugin](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Change requests can now be auto-closed without requiring you to install the Change Management - State Model \[Legacy\] plugin.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[Use DEX Desktop Assistant](https://www.servicenow.com/docs/access?context=use-dex-desktop-exp&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

By default, the Desktop Assistant home page now has two sections: My resources and Quick links. My resources includes Device health check and Network test cards, while Quick links includes Employee Center and Outages cards.

-   **[Modified Devices page](https://www.servicenow.com/docs/access?context=dex-workspace-devices-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   The device view is now optimized and segregated into two tabs based on the user persona. The **All devices** tab is for DEX operators, and the **Devices by ACC status** tab is for DEX operators and DEX admins.
    -   The application performance tab in the Device page has been enhanced. Filter performance for installed apps and web apps by date and time, and view the performance metrics for the last seven days.
    -   Access the performance page to view the performance and details of both installed and web applications.
    -   Filter the active devices to view only the devices that were active in the last five minutes.
-   **[Updated landing page](https://www.servicenow.com/docs/access?context=dashboard-cards&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The world map in the **Devices** section on the DEX landing page now shows the devices list instead of users list. The Impacted Devices card now shows the count of impacted users based on the alerts of both the devices and the applications running on that device.

-   **[Updated users link reference](https://www.servicenow.com/docs/access?context=devices-form&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The user link now redirects to Users page in Service Operations Workspace.

-   **[Changed device alerts](https://www.servicenow.com/docs/access?context=user-health-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View alerts for both your device and its applications in the Alerts section of the Devices page.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Transformed chargeback eligibility rules into technical formulas to determine the eligibility or ineligibility of a selected transaction for chargeback.

-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard by adding new questions and updating existing questions.


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#section_gsl_nw5_vyb)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 25.2 revision changes.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Connect documents on external cloud](https://www.servicenow.com/docs/access?context=upload-versions-external-cloud&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Upload your files directly to an external cloud \(including multiple versions of the document\).

-   **[Permissions for external cloud files](https://www.servicenow.com/docs/access?context=document-configuration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Set the sharing permissions on your external cloud files.

-   **[Authenticate personal accounts on external cloud](https://www.servicenow.com/docs/access?context=personal-authentication-documents&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Implement personal token-based authentication for an external cloud so that you can verify user-specific access, audit trails, and compatibility with existing and future integrations.

-   **[Connect file extensions](https://www.servicenow.com/docs/access?context=upload-versions-external-cloud&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Link any Google Drive file to a document record by selecting a provider and entering the file URL All file extension are now supported.

-   **[HTML to PDF Conversion](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Specify an image retrieval timeout for HTML to PDF conversion.

-   **[Document classification](https://www.servicenow.com/docs/access?context=share-document-link&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Limit public sharing based on a document's classification.

-   **[PDF generation](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Generate a PDF with accessibility for regulated markets.

-   **[Property value for digital signature using CAC or PIV smart cards](https://www.servicenow.com/docs/access?context=property-value-cac-piv-signing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Specify the method used to identify and validate the user who has signed the PDF using the property value.

-   **Document summarization**

Use AI to generate summaries for feedback, disclaimers, and usage tracking in PDFs and Microsoft Word files.

-   **[Document Services Framework for Microsoft OneDrive](https://www.servicenow.com/docs/access?context=onedrive-spoke-document-services-framework&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Retrieve the list of files and folders based on the given search query from Microsoft OneDrive.

-   **[Document Services Framework for Google Drive](https://www.servicenow.com/docs/access?context=google-drive-spoke-document-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Retrieve the list of files and folders based on the given search query from Google Drive.


</td></tr><tr><td>

ERP Semantic Mining

</td><td>

-   **[ERP Customization Mining application name change](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

The name of the ERP Customization Mining application has been changed to ERP Semantic Mining.


</td></tr><tr><td>

Encryption

</td><td>

-   **[Field Encryption Enterprise](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) API**

Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[Updates to GlideEncrypter functionality](https://www.servicenow.com/docs/access?context=glideencrypter-deprecation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The GlideEncrypter API has been updated to use AES256-GCM encryption via the Key Management Framework. If needed, your instance can be changed to use legacy 3DES encryption, but this task can only be done by ServiceNow support.

-   **[Disable GlideEncrypter on your instance](https://www.servicenow.com/docs/access?context=check-3des&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

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

-   **[Enterprise Asset Management demo data migration](https://www.servicenow.com/docs/access?context=install-eam-demo-data&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

All Enterprise Asset Management demo data has migrated from the Enterprise Asset Management application to either the EAM Demo Data application or Indoor Mapping for Assets application. The EAM Demo Data application contains all Enterprise Asset Management demo data except for indoor mapping-related demo data, which is now included in the Indoor Mapping for Assets application.

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Starting from the Enterprise Asset Management version 9.1.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-enterprise-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Starting from Enterprise Asset Management version 9.1.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Event Management

</td><td>

-   **Automated regex generation**

Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.

-   **Support for OAuth authentication method in Kafka connector**

Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, allowing you to securely connect and manage access without storing or sharing static credentials.

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

-   **[Sitemap support in the Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://www.servicenow.com/docs/access?context=create-content-crawl-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://www.servicenow.com/docs/access?context=review-crawl-ext-cont-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://www.servicenow.com/docs/access?context=atlassian-confluence-cloud-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


-   **[Analytics for external content connectors](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-microsoft-onedrive&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-mspo&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which enables you to specify a custom web source or select a predefined one.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Capacity and Reservations Management](https://www.servicenow.com/docs/access?context=configuring-capacity-management&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use the aggregated schedules of all agents of a territory to allocate resources until a specified cut-off date, after which predicted capacity can be used for bookings. This feature optimizes resource utilization and capacity management for a territory, which helps ensure that business services remain available without overburdening resources.

-   **[Google Maps APIs for  Field Service  capabilities](https://www.servicenow.com/docs/access?context=google-maps-api-keys&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you create a Google API key after March 2025, you must upgrade to a supported ServiceNow release version to verify compatibility.

-   **[Smart Assessment for Field Service](https://www.servicenow.com/docs/access?context=configuring-smart-assessment-questionnaire&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use Smart Assessment for Field Service to do the following:

    -   Streamline asset identification and data entry by scanning and capturing barcode values directly within a work order questionnaire.
    -   Configure a predefined range for numeric inputs to minimize errors and help ensure data accuracy.
    -   View completed questionnaires in the workspace.
    -   Create follow-up work order tasks from a work order questionnaire based on the responses.
    -   Allow users to retry or replace an attachment if the upload is unsuccessful.
-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Migrates data from the Work Parameter table to the Resource Schedule Attribute table for each technician, confirming that work parameters align with the new schedule attributes.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Overview of the Dispute Management workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Track the progress of the investigation workflow intuitively with a redesigned user interface that presents each transaction within a dispute case using a clear, process-based layout. This new layout visualizes the distinct stages of the investigation workflow, Investigate, Chargeback, and Closure, which enhances visibility and dispute management efficiency.


-   **[Managing disputes integrated with Mastercard](https://www.servicenow.com/docs/access?context=work-on-disputes-integrated-with-mc&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Integrate the Dispute Management workflow with subflows that communicate with Mastercom, supporting an end-to-end dispute life-cycle from raising an initial dispute to final resolution.

-   **[Unified dispute intake experience](https://www.servicenow.com/docs/access?context=dispute-intake-overview&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US#section_c13_crs_bdc)**

The dispute intake process has been streamlined to provide a clear, intuitive experience for customers and dispute agents, resulting in faster resolution and reduced manual effort. A unified interface now allows cardholders, account holders, and agents to raise disputes for both card and non-card \(ACH\) transactions seamlessly.


</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **[Added field to Financial transaction table](https://www.servicenow.com/docs/access?context=fso-core-banking-tables&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Added the **Payment Card** field to the Financial transaction \[sn\_bom\_transaction\] table as part of the Payment card application.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Direct action calls removed from Generative AI Controller](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

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

-   **[Active goals](https://www.servicenow.com/docs/access?context=defining-goals-using-goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed in the **Goal** and **Parent goal** reference fields across all applicable tables.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Goal system properties](https://www.servicenow.com/docs/access?context=components-installed-with-goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US#section_myd_rzy_fyb)**

Users with the sn\_gf\_goal\_admin role assigned can update goal-specific system properties:

    -   **sn\_gfa.weeklyCheckInDayToMapMonth** - Defines the end day of the week used for mapping weekly target breakdowns to a month. The default value is Friday.
    -   **glide.ui.sn\_gf\_goal\_target\_activity.field** - Enables activity stream for fields of the targets.
    -   **sn\_gfa.target\_breakdown\_decimals** - Sets the number of decimal places displayed for target values when generating target breakdowns. The default value is 2.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Shipment asset table label](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Starting from the Hardware Asset Management version 14.0.0, the Shipment asset \[sn\_itam\_common\_m2m\_shipment\_asset\] table label has been renamed to Shipment line \[sn\_itam\_common\_m2m\_shipment\_asset\].

-   **[Shipment quantity field on the Shipment Details form](https://www.servicenow.com/docs/access?context=view-hardware-asset-shipments&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

With Hardware Asset Management version 14.0.0, a new field **Shipment quantity** has been added to the Shipment Details form. The **Shipment quantity** field displays the quantity of assets shipped for the shipment record.


</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   **[Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](https://www.servicenow.com/docs/access?context=configure-care-team-portal&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

The process for embedding Care Team Portal into your EMR system has been streamlined to enable more efficient launch context configuration.

The portal now supports capturing launch context tokens across multiple launches within the same Hyperspace session when embedding Care Team Portal into Epic's Hyperspace. Previously, only tokens captured from the initial launch were displayed.

The FHIR endpoint is now retrieved dynamically, eliminating the need to embed it directly in the Single Sign-on Script.

-   **[Setting up roles and responsibilities for Healthcare Operations users](https://www.servicenow.com/docs/access?context=cto-setting-up-roles-responsibilities&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

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

-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://www.servicenow.com/docs/access?context=available-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Note the following new Pattern improvements using version 1.29.0:

    -   [IBM Hardware Management Console \(HMC\)](https://www.servicenow.com/docs/access?context=ibm-hmc-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US): additional fields in IBM Frame \[cmdb\_ci\_ibm\_frame\] and IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\] tables
    -   [Dell PowerMax storage](https://www.servicenow.com/docs/access?context=emc-powermax-discovery-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [Pure Storage FlashArray](https://www.servicenow.com/docs/access?context=flasharray-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [NetApp Server and Cluster](https://www.servicenow.com/docs/access?context=netapp-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [AWS Auto Scaling groups](https://www.servicenow.com/docs/access?context=aws-auto-scaling-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US): The relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**
-   **[Employ Tag-based mapping in the Service Mapping Workspace](https://www.servicenow.com/docs/access?context=map-tag-based-services-workspace&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Easily view data and create new tag-based services through an enhanced workspace that includes a dedicated dashboard for managing your tag-based services.

-   **[Name updates in Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

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
-   **[Benefit from an updated, curated selection of application service candidates in Service Mapping](https://www.servicenow.com/docs/access?context=sm-dashboard&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

If you have ITOM Content Service installed, you can view an enhanced selection of Application Service Candidates \(ASCs\) that provides more accurate and useful information, with an automatic filter applied to hide irrelevant and non-essential components.

-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://www.servicenow.com/docs/access?context=automate-certificates-ejbca-acme&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://www.servicenow.com/docs/access?context=discover-root-certificate-browser&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Kubernetes Visibility Agent \(KVA\)](https://www.servicenow.com/docs/access?context=acc-kubernetes-visibility-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

KVA performs continuous discovery to detect changes on resources in a Kubernetes cluster and updates the CMDB with the latest data.

Starting with KVA version 3.11.0, and Informer version 2.5.0, absent namespace CIs aren’t deleted automatically. Create a scheduled job to remove them.

Starting with KVA version 3.11.0, and Informer version 2.5.0, map application services based on traffic connections between the workloads in Kubernetes, by using istio and linked service meshes or the DaemonSet service.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://www.servicenow.com/docs/access?context=create-an-http-classifier&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.

-   **[Automated Certificate Renewal](https://www.servicenow.com/docs/access?context=automated-certificate-renewal&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


</td></tr><tr><td>

Identity

</td><td>

-   **[Access analyzer](https://www.servicenow.com/docs/access?context=access-analyzer&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Display the Security data filter that is in the **Applied** or **Undefined** status in the Access Analyzer results. Access Analyzer also supports the new criteria in ACLs that is controlled by reference.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


</td></tr><tr><td>

Impact

</td><td>

-   **[The outcome summarization Now Assist skill is now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

This skill is automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[GenAI-powered Root Cause Summary](https://www.servicenow.com/docs/access?context=generative-ai-root-cause-anal&version=zurich&pubname=zurich-impact&ft:locale=en-US)**
    -   Use the dynamically generated Root Cause Analysis \(RCA\), which is readily available in the RCA History page. RCA is available not only for alerts but also for the Critical or Warning scenarios of the performance category. This feature is a change to the existing functionality and is delivered dynamically.
    -   The core Root Cause Correlation functionality is being offered under the revised name of Root Cause Analysis to ensure product consistency.
-   **[Artificial Intelligence Readiness Assessment Accelerator](https://www.servicenow.com/docs/access?context=artificial-intelligence-readiness-assessment&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

The content and flow of this Accelerator has been streamlined to provide a clearer assessment and more targeted guidance on your readiness to adopt ServiceNow Generative AI capabilities \(Now Assist\).

-   **[Jumpstart Your ServiceNow AI Journey Accelerator](https://www.servicenow.com/docs/access?context=jumpstart-snow-ai-journey&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

This offering is now available across all packages, and includes clearer guidance on how customers can leverage ServiceNow’s AI capabilities to achieve their organizational goals and objectives.

-   **[Use Guided Setup for Impact Store Application configuration](https://www.servicenow.com/docs/access?context=guided-setup-impact-in-app&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Use automated registration, the preferred method, to initiate the connection and registration to the Impact Delivery Instance provider instance in one combined step.


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Incident task record behavior changes](https://www.servicenow.com/docs/access?context=create-incident-task&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When an incident task is closed, you can no longer edit the field values in the incident task form. Disabling the fields helps prevent any further updates or modifications to closed incident tasks, reducing audit risks.

-   **[Incident and problem workflow changes](https://www.servicenow.com/docs/access?context=working-incident-record-form&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When a problem record is linked to an incident or multiple incidents, the incident and problem workflow has the following enhancements:

    -   When a fix or workaround is shared from the problem record, an event is added in the activity stream of the incident record as work notes. The event includes a brief description of the provided fix or workaround and a link to the problem record.
    -   When a Known Error \(KE\) article is linked to the problem record, an event is added in the activity stream of the incident record as work notes. The event includes the links to the problem record and the KE article.

</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **Admin role dependency**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Viewing multiple records at once in the Equipment Model Manager](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[New debugging property for Stream Connect](https://www.servicenow.com/docs/access?context=kafka-subscriptions-statistics&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Enable more detailed logging in the Stream Connect logs with the **glide.ih.kafka.stream\_connect.debug** property. This property replaces the **glide.ih.kafka.debug.consume** property.

-   **[Spoke Generator license changes](https://www.servicenow.com/docs/access?context=spoke-builder&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Starting with Zurich, the Spokes list page and Spoke details pages are a part of the ServiceNow Integration Hub Starter Pack. To create a spoke using OpenAPI or Postman collection specification or Now Assist, you need a ServiceNow Integration Hub Professional license in your prod and sub-prod environments.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **[Dynamic artifact detection](https://www.servicenow.com/docs/access?context=lw-dynamic-artifact-detection&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Dynamic artifact detection enables Localization Workspace to identify all translatable content, including your custom artifacts. From version 1.1.0.

-   **[Status synchronization](https://www.servicenow.com/docs/access?context=lw-status-synchronization&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

With status synchronization, you see the same status for your translation request in Localization Workspace as you see for the corresponding project in Localization Framework \(Submitted, In progress, Complete\). From version 1.1.0.


</td></tr><tr><td>

MID Server

</td><td>

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[Enhancements to MID Server logging and JFR](https://www.servicenow.com/docs/access?context=r_MIDServerTroubleshooting&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

MID Server logging has been improved with log backups that are preserved in a compressed format on local host with option to fetch to the instance. You can enable JFR logs every four hours and backup JFR files for a set time.

-   **[MID Server has improved performance during heavy discovery load](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

MID Servers no longer have performance degradation due to script include cache misses when using large amounts of worker threads.


</td></tr><tr><td>

Mentoring

</td><td>

-   **[Create a Mentoring program](https://www.servicenow.com/docs/access?context=create-mentoring-pgm&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The multiple mentoring program enables mentor admins to configure multiple programs that can run at the same time. It enables admins to restrict access based on employee criteria. The multiple mentoring program enables employees to choose and enroll in available mentoring programs, edit their preferences, search for mentors, and send connection requests.

To make a program visible in the Mentoring app, admins need to configure programs with the following information:

    -   Short description
    -   Long description
    -   Employee criteria

</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Enhanced native features in hybrid web screens](https://www.servicenow.com/docs/access?context=url-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Enhanced native features in hybrid web screens that support functionality such as native search, quick actions, and customizable welcome messages within hybrid screen launcher or header tabs.

-   **[Enhanced chat push notifications](https://www.servicenow.com/docs/access?context=using-enhanced-chat-mobile&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

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

-   **[Email digest for multiple target records](https://www.servicenow.com/docs/access?context=configure-email-digest&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The email digest now supports both single or multiple target records within a set time interval.

-   **[Notification preferences](https://www.servicenow.com/docs/access?context=create-notification-filter-configuration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Enables admins to control the list of notifications displayed for users under the advanced notification preferences.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Using Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=using-now-assist-readiness-evaluation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI- Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable translation settings is now a multilingual service in the Now Assist Admin console.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Create an external AI agent with the Agent2Agent protocol](https://www.servicenow.com/docs/access?context=create-a2a-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Generate resolution plans](https://www.servicenow.com/docs/access?context=resolve-requests&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now takes related records into account when planning next steps. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) shows suggested next steps and reruns after work is done. [Process images for new tasks](https://www.servicenow.com/docs/access?context=images-tasks&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now links to the created task record upon creation and includes certain metadata from the image.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Platform Request status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Understand the Now Assist AI agents](https://www.servicenow.com/docs/access?context=understand-na-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The base reflection prompt has been replaced with the ReAct Orchestrator prompt, introducing a Route scheduling mode when an agent needs assistance from another agent during execution.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


-   **[Review and complete actions on requests using the Request Status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The ticket status AI agent has been renamed to the request status AI agent. Request details include an AI-generated summary of the most recent comments on a request. Performance has been improved.

-   **[Confirm your web search tool provider data policies](https://www.servicenow.com/docs/access?context=add-web-search-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

If you select Google as your web search provider for web search AI agent tools, Google uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow AI Platform instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://www.servicenow.com/docs/access?context=version-control&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool. After an existing tool is added, you can change it to suit the specific needs of an AI agent.

-   **[Now Assist AI agents reference](https://www.servicenow.com/docs/access?context=na-aia-reference&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the Agent properties \[sn\_aia\_property\] table.


</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for App Engine

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for CMDB

</td><td>

-   **[View CI attribute descriptions on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Create a CI using Now Assist](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Verbal interaction with this feature has improved. Occasionally, you might need to create a CI manually. To help you, the CI creator agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

-   **[Getting advice from Now Assist on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-governance&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

To help users understand the value of each step in the process, responses now include richer context. The CMDB Governance agentic workflow supports administrators and service owners by improving CMDB data governance. Before starting in on each governance task, the workflow presents the reasons for the task to help you better understand the importance and benefits of the activity. The objective is to ensure that CMDB data is accurate and complete so that users can trust the data.

-   **[Use Now Assist to search the CMDB for CIs](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Verbal interaction with this feature has improved. Users can now select the CI inline when multiple CIs are returned as matches. A summary of the CI now appears in the conversation. The CMDB search agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information that you provided. The workflow can infer CI relationship data to generate an appropriate query.

-   **[View CI information with the Now Assist CI summarization skill](https://www.servicenow.com/docs/access?context=na-cmdb-agent-ci-summarizer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Verbal interaction with this feature has improved. You can now view a concise summary of the key CI data by selecting the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

-   ****

Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

-   **[Fix SGC import set issues with the Now Assist SGC diagnosis skill](https://www.servicenow.com/docs/access?context=now-assist-sgc-diagnose&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Verbal interaction with this feature has improved. You can now diagnose a failed import set that is associated with a Service Graph Connector to get a summary of the errors and recommendations for resolving the issues.


</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Configure, Price, Quote \(CPQ\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   **[Changes to Complaint Case AI agent collection](https://www.servicenow.com/docs/access?context=accelerate-complaint-case-handling&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Updates have been added to the Complaint Case playbook to work better with the Complaint Case AI agent:

    -   Triage displays complaint details and enables a human agent to identify and request missing information.
    -   Complaint‑specific case summarization is available directly within the playbook.
    -   Replace research case task activities with case tasks list activity.
-   **[Enhancements in the Sentiment analysis dashboard](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**
    -   Sentiment analysis dashboard support has expanded to include interaction records, and positive and negative sentiment drivers have been consolidated into a single Sentiment Drivers view.
    -   The top negative assignment group and number of cases by channel visualizations have been merged into the new Impact Explorer visualization for streamlined analysis.
    -   Widget placement in the Workforce Optimization dashboard has been optimized for accessing insights and trends across interfaces.
-   **[Enhancements in Trending topics dashboard](https://www.servicenow.com/docs/access?context=view-trending-topics-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**
    -   The Accounts, Products, Assignment Groups, and Channels graphs have been consolidated into the Impact Explorer card.
    -   Search and pagination have been added to the list header.
    -   The Historical trends resurfacing graph has been added the Trending topics dashboard to show historical trends at a glance.
    -   Trending topics have been expanded beyond the top 10 results to provide deeper insight into emerging patterns.
    -   The trending topics widget has been added in the Workforce optimization dashboard as the **AI insights** tab.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Enhancement in case summarization skill flow](https://www.servicenow.com/docs/access?context=case-summarization-generation-in-now-assist&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

The **Define trigger** step has been added to the case summarization flow. This step enables admins to choose between the User Trigger option, where users select a button to generate a summary, and the Automatic Trigger option, where summaries are automatically generated based on specified conditions.

-   **[Enhancement in email reply recommendation skill](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.

-   **[Unified admin experience for Now Assist skills](https://www.servicenow.com/docs/access?context=customizing-now-assist-skills&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Skills cloned in Now Assist Admin console can now be edited in Now Assist Skill Kit. This update unifies the admin experience across Now Assist Admin and Now Assist Skill Kit, enabling users to add headers, configure prompts, and manage Now Assist skills in one location. The migration supports case summarization and resolution notes generation.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Display sentiment scale in case list view](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Sentiment scoring has been added to both the case record page and list view across cases, giving agents immediate visibility into the emotional tone of customer interactions. The sentiment scale ranges from very positive, positive, neutral, negative, to very negative.


-   **[Multilingual support](https://www.servicenow.com/docs/access?context=now-assist-csm-supporting-info&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enhanced multilingual support in chat summarization, resolution notes, and knowledge generation. Leveraged native multilingual LLMs for improved fluency and domain specificity, addressing translation inconsistencies across Tier 1 and Tier 2 languages.


-   **[Suggested steps in the Recommended Actions tab](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

View the suggested steps on the **Recommended Actions** tab in the contextual side panel. If suggested steps are available for a case, Now Assist for CSM generates and displays these steps in a card at the top of the **Recommended Actions** tab.

-   **[KB generation skill configuration enhancement](https://www.servicenow.com/docs/access?context=now-assist-csm-configuring&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

The **Is Template** field on the KB generation skill configuration record is enabled by default. With the skill\_builder.admin role, you can copy or clone the KB generation skill and customize the prompt in the skill kit.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for FSM

</td><td>

-   **[Create Work Order AI agent performance improvements](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

The Create Work Order AI agent was optimized to reduce latency and improve response times. Inter-agent communication was streamlined to minimize redundant processing during work order creation.

-   **[Removed prompt headers](https://www.servicenow.com/docs/access?context=cust-now-assist-fsm-wot-summarization-skill&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

The prompt headers have been removed from the work order summarization skill to support third-party large language models. You can now customize prompts via a hyperlink to the Now Assist skill.


</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Disputes intake via Virtual Agent](https://www.servicenow.com/docs/access?context=exploring-now-assist-for-financial-services-operations-fso&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US#section_ir3_pn5_lbc)**

Disputes intake via Virtual Agent has the following updates:

    -   Questions presented to the user for disputes will follow the dispute questionnaire in the disputes playbook.
    -   Bypass inferring answers to certain questions so that customers provide answers directly, ensuring the correct dispute category and dispute reason are determined.
    -   Supports ACH disputes, Disputes intake via Virtual Agent including submission of the Written Statement of Unauthorized Debt \(WSUD\).
    -   Checks if the disputed transaction is already part of an existing case.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Functional change](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The resolve HR cases agentic workflow has been broken down into three agentic flows:

    -   [Predict service and transfer HR cases agentic workflow](https://www.servicenow.com/docs/access?context=predict-transfer-hrcase&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
    -   [Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
    -   [Resolve critical HR case agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolve-critical&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)

-   **[Flow name](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The resolve noncritical HR cases workflow has been renamed to the resolve HR cases workflow.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Four AIOps AI agents have been removed from the analyze alert impact agentic workflow because they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[AIOps LEAP rebranding](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation.

-   **[Service Operations Workspace \(SOW\) Integration](https://www.servicenow.com/docs/access?context=view-and-use-aiops-leap-playbooks-in-sow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Playbooks appear in SOW module.

-   **[Data Range Display](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The AIOps LEAP landing page shows analyzed data date range for automation teams to be aware of time-ranges of analysis.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The Incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The voice AI demo agents have been renamed as primers.

-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

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

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization

</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-summarize-case&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Summarization now includes data from extended practice area tables, providing context‑rich summaries for your legal requests and matters.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Operational Sustainability Management Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Order Management

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Retail Service Management \(RSM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications \(SOMT\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

-   **[Resolve a security incident](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   **[ppm.ai\_project\_manager\_agent user role](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The agentic workflow, agents, and scheduled jobs are configured to run under the new ppm.ai\_project\_manager\_agent user role instead of the administrator account.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Third-party Risk Management \(TPRM\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://www.servicenow.com/docs/access?context=auto-complete-suggestion-types-na-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.

-   **[Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=now-assist-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=now-assist-catalog-ordering-gr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Configure use case mappings for metadata and obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-usecase-mappings-me&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The Now Assist powered conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
The conversational search feature does not support searching within contract documents that are scanned PDFs.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Enhanced Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The manage contract repository agentic workflow has been optimized for enhanced performance. It now utilizes a single agent, the Contract Repository AI agent to extract both contract metadata and obligations from signed contracts, and retrieve required information to calculate the contract reminder date.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **[Extract metadata from signed contracts automatically](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the AI agents in the manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://www.servicenow.com/docs/access?context=metadata-extraction-use-case&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case is available in the base system.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Tools used by the document and visual insights AI agent are consolidated to improve performance.

-   **[Changes to limitations](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-limitations&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The file size limit for uploading a file using the attachment summarization feature is changed from 10MB to 20MB.

-   **[Document Intelligence for Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=add-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The document and visual intelligence capabilities used to leverage extraction, question answering, and summarization capabilities for skills created with Now Assist Skill Kit are available to users with the appropriate role\(s\).

-   **[Now Assist in Document Intelligence skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading: Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes to limitations](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-limitations&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The page count limit decreases to 20 pages per file for an extraction based on a use case with a table defined.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **Merged skills**

Document data extraction and document Q&amp;A capabilities are available in a single Extract information from documents skill.

    -   The Extract information from documents skill is available in the list of Platform skills in the Now Assist Admin console.
    -   Data extraction and document Q&amp;A capabilities can be set up for the same use case.
    -   Agents can review the AI predictions for the fields, tables, and questions in the same task.
-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Leverage added tools that enable the AI agent to display the extracted data and to look up existing use cases or create use cases based on descriptions and document attachments.

-   **[Changes to limitations](https://www.servicenow.com/docs/access?context=now-assist-document-intelligence-limitations&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The limitations set for Now Assist in Document Intelligence properties are updated to support processing larger documents.

    -   DOCX files are supported for information extraction.
    -   The page count limit is 200 pages per file If image mode is turned off for the use case. If image mode is turned on, the page count limit is 10 pages per file.
    -   The file size limit is 20 MB.

</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[View recommended actions](https://www.servicenow.com/docs/access?context=expl-view-recommended-actions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://www.servicenow.com/docs/access?context=qg-supported-query-operations&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://www.servicenow.com/docs/access?context=querygen-segments&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for indicator sources or modules on domain-separated instances.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Dashboard and data visualization export skill is active by default](https://www.servicenow.com/docs/access?context=export-db-dv-now-assist-panel&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) \(January 2026\)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 5\): If this skill was previously unconfigured, it is turned on automatically \(the skill was never configured and turned on, then turned off again\). If the skill was previously turned on, then off, it remains inactive.

-   **[Query Generation skills are active by default](https://www.servicenow.com/docs/access?context=enable-query-generation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

If the Generative AI Controller plugin is activated, the skills for Query Generation are activated by default. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Greater visibility into the Query Generation process](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

When you call Query Generation from AI Data Explorer or another application, you see each state that the query and response goes through before completing.

-   **[Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Query Generation supports related table conditions and dot-walking in queries.

-   **[Get insights and visualizations for Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Ask AI Data Explorer information about Workflow Data Fabric data and get insightful responses. You must first add the Workflow Data Fabric tables to the Query Generation Semantic Table Configuration table.

-   **[Use database views in queries](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Generate visualizations or ask AI Data Explorer about data kept in database views, like SLA data. You have to add the database views to the Query Generation Semantic Table Configuration table.


-   **[Add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Choose which tables your users can query with generative AI for data analysis.

-   **[Monitor the health of the Query Generation back end](https://www.servicenow.com/docs/access?context=querygen-health-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

View the state of Now Assist for Platform Analytics LLM, plugins, system properties, components, and dependent products.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Conversational Platform Now Assist skills are active by default](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://www.servicenow.com/docs/access?context=web-search-requestor&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Performance improvements in subflows for on-call notifications](https://www.servicenow.com/docs/access?context=on-call-new-trigger-engine&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The following performance enhancements are available for on-call notifications when subflows are used:

    -   On-call notifications are sent to multiple channels such as SMS or email simultaneously instead of sending it sequentially.
    -   When the **com.snc.on\_call\_rotation.new\_trigger\_engine** property is set to true, the on-call subflows are processed via the Flow runner queue. The on-call subflows that are marked as High priority are processed faster via a Flow runner queue especially when multiple events are triggered at the same time and are in the process queue.
    -   Reminder notifications are also sent to users when the instance is upgrading.
-   **[Enhanced on-call trigger rules to support subflows](https://www.servicenow.com/docs/access?context=on-call-scheduling-subflows-overview&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The on-call trigger rules form is enhanced to trigger a subflow when the trigger rule is executed. You can enable and select a specific subflow for a trigger rule.


</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **Admin role dependency**

Several new granular admin roles have been added, which enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than 1 CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

The Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **Admin role dependency**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[IT Discovery for Operational Technology \(OT\) Networks](https://www.servicenow.com/docs/access?context=discovery-for-operational-technology&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

The Discovery for Operational Technology plugin has been renamed IT Discovery for OT Networks.

-   **[Operational Technology Manager roles](https://www.servicenow.com/docs/access?context=assign-operational-technology-manager-roles&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

The following changes have been made to Operational Technology Manager roles:

    -   Users assigned the Operational Technology Manager Editor \[cmdb\_ot\_editor\] role or Operational Technology Manager Admin \[cmdb\_ot\_admin\] role cannot edit IT configuration items \(CIs\). Users with these roles can only edit or delete OT CIs.
    -   Users who aren't assigned an OT role cannot view OT records in the following CMDB tables:
        -   IP Address \[cmdb\_ci\_ip\_address\]
        -   Network Adapter \[cmdb\_ci\_network\_adapter\]
        -   Serial Number \[cmdb\_serial\_number\]
    -   The Operational Technology Editor \[cmdb\_ot\_editor\] role contains the cmdb\_manual\_ci\_ire\_access role to support manually creating an OT CI in the Industrial Workspace.

</td></tr><tr><td>

Order Management

</td><td>

-   **[Changes to OM integration with SPM](https://www.servicenow.com/docs/access?context=configure-site-project-product-offering&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Use OM integration with SPM to create program, reuse program, create site project and reuse site project in the SPM.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Select whether to drill down to Platform Analytics or Core UI lists](https://www.servicenow.com/docs/access?context=visualization-drilldown-in-config-ws&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Decide whether data view chart interactions for data visualizations on an instance drill down to Platform Analytics or Core UI record lists. This choice applies only on the Platform Analytics experience.

-   **[View usage information in the dashboards library](https://www.servicenow.com/docs/access?context=dashboards-for-admin-users&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

For analytics managers, the dashboard library now contains usage statistics, such as the number of dashboards not viewed in one year and the number of dashboards deactivated for more than three months.

-   **[Export data visualizations from dashboards to PNG and JPEG](https://www.servicenow.com/docs/access?context=export-data-vis-from-dboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Export individual data visualizations as a viewer to a graphic file.

-   **[Platform Analytics experience is supported even when Next Experience UI is disabled](https://www.servicenow.com/docs/access?context=data-migration-perform&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

You can migrate to Platform Analytics even if Next Experience isn’t enabled. Core UI dashboards are embedded in iframes.

-   **[Migration Center changes](https://www.servicenow.com/docs/access?context=data-migration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**
    -   Dashboard owners can perform partial migration on their own dashboards.
    -   Geomap migration supported.
    -   Interactive filter check box option.
    -   Export to CSV from lists is supported.
-   **[Data visualizations and filters support Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=workflow-data-fabric&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Perform data analysis on external data fabric sources.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Activate playbooks without a trigger](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **[Implement playbooks that are callable by a scriptable API](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **[Decision activity enhancements](https://www.servicenow.com/docs/access?context=create-a-decision-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

User experience improvements to decision activities:

    -   In the Board view, select the branch or Start rule icon on a decision activity card to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://www.servicenow.com/docs/access?context=add-configure-activity&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Improvements to the rationalization process of control objectives](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Processing activity tab](https://www.servicenow.com/docs/access?context=processing-activity-tab&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The revamped Processing Activity overview page provides a unified dashboard that displays key compliance and risk metrics, such as risk scores, compliance scores, and criticality scores. This update makes it easier for privacy managers and analysts to assess the status of each processing activity, track open issues, and prioritize actions.


-   **[Layout for processing activity record view](https://www.servicenow.com/docs/access?context=processing-activity-homepage&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The vertical layout of a processing activity enables you to see the information in a top-down linear flow. With this layout, you can see the sequential representation of a data processing workflow.

-   **[Privacy management home page](https://www.servicenow.com/docs/access?context=privacy-mgmt-ws-privacy-compliance-manager&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The enhanced Privacy Management home page now has dedicated tabs for Processing Activity, Risk and compliance, Operations, and Privacy Cases. This updated layout helps to improve readability by organizing your reports into clearly defined sections.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Support minor changes to published product offerings and specifications](https://www.servicenow.com/docs/access?context=minor-updates-published-offerings-specs&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Make minor changes to published versions of a product offering or specification, without creating a version. Minor updates include changes such as modifying the product offering display name, description, or product image.

-   **[Configurable product offerings](https://www.servicenow.com/docs/access?context=som-create-product-offering&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

The Create Product Offering form, used when creating product offerings, has two new options. The **Configurable** option indicates that the product offering is configurable and that it can be customized by agents and customers using the CPQ Configurator. The **Enable ramps** option indicates that price ramps can be defined for a configurable product.

-   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://www.servicenow.com/docs/access?context=export-import-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://www.servicenow.com/docs/access?context=export-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://www.servicenow.com/docs/access?context=import-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Enhancements to Grants Management: Program Setup](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

In the Grants Management: program setup, grant program managers can now add new points of contact for the applicants to the grants program in the Define Program stage. In the Publish Program stage, new fields have been added for program announcement removal. Grants program managers can now set grants programs to auto-remove at a defined date, and set application close to disable new applications from being submitted through the Grants Management portal.

-   **[Enhancements to Grants Management portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-grants-mgmt-portal&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

Enable grant program managers to turn off new grant proposal submissions after the proposal close date. Applicants can no longer submit proposals after the proposal close date, keeping the process on schedule and helping prevent late submissions from being reviewed.

Enable applicants to review and download the results letter and merit review summary \(where applicable\) of their grants application, as well as accept or decline their award, all within the new **Results** tab of the Grants Management portal. Notify constituents about a pending award decision through the portal.


-   **[Constituent Service Dashboard Migration to Platform Analytics](https://www.servicenow.com/docs/access?context=constituent-services-dashboard&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when you load or upgrade to the Zurich release. The dashboard migration to Next Experience enables you to visualize historical and real-time process statistics in role-based dashboards. Access the new dashboard by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


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
-   **[Tasks widget](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The overview page of a regulatory alert includes a newly added Tasks widget that enables you to get more visibility into related activities. This widget displays the total number of associated action tasks and change tasks that are linked to the specific regulatory alert. By using this widget, you can assess the level of effort that is required for compliance.

-   **[Workflow of regulatory task](https://www.servicenow.com/docs/access?context=reg-change-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

A regulatory task progresses through the following states:

    -   New
    -   Work In Progress
    -   Implementation
    -   Awaiting Approval \(optional\)
    -   Completed
While in the Implementation state, requesting approval is optional. If all associated action tasks are completed, the regulatory task can be closed directly from the Implementation state without requiring additional approval.

-   **[Workflow of source document import task](https://www.servicenow.com/docs/access?context=reg-change-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

A source document task progresses through the following states:

    -   New
    -   Ready to Import
    -   Work In Progress
    -   Implementation
    -   Completed.
-   **[Create action tasks](https://www.servicenow.com/docs/access?context=manage-reg-action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

You can create action tasks for a regulatory task when the task is in any of the following states:

    -   New
    -   Work in Progress
    -   Implementation
You can now break down a regulatory task into smaller, manageable components so that you can more efficiently track and execute the required activities. You can plan, assign, and monitor tasks now in a structured manner that supports your compliance objectives and regulatory requirements.


</td></tr><tr><td>

Return Merchandise Authorization

</td><td>

-   **[Enhancements in the RMA case flow](https://www.servicenow.com/docs/access?context=return-merchandise-authorization&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Streamline the sales return process by enabling agents to initiate, track, and close RMA cases for install base items directly within the Agent Workspace. It also bridges the gap between self-service and full support.


</td></tr><tr><td>

Security Center

</td><td>

-   **[Auditor checks](https://www.servicenow.com/docs/access?context=auditor&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The Review Public Knowledge Bases and Review Public Knowledge Base Articles checks use global API calls, so they've been added in the Global scope.

-   **[Security Center](https://www.servicenow.com/docs/access?context=sec-center-v2&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) Theming for Security Center**

Security Center banners and Cascading Style Sheets CSS elements have been updated to conform to any instance-wide themes you apply.

-   **[Updated first time user experience](https://www.servicenow.com/docs/access?context=sec-center-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Security Center has been updated to provide guidance to understand what the tool can do and how to use it. This redesign is tailored to assist both new and infrequent users of Security Center.

-   **Hardening settings updates**

Updated the Security Hardening tool with the latest Instance Security Hardening Settings baseline V6.

-   **[Security Hardening tool Updates](https://www.servicenow.com/docs/access?context=security-hardening-settings&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The security Hardening tool has been updated to the latest Instance Security Hardening Settings V7.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Incident Response Other Records](https://www.servicenow.com/docs/access?context=security-incident-response-other-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Add  multiple ITSM incidents, problems, or change requests to a security incident for which multiple IT actions are needed. For more information, see the "Link multiple ITSM incidents" section.

-   **[Modify attachments of a closed security incident](https://www.servicenow.com/docs/access?context=t_ClosingSecIncidents&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You cannot modify the attachments of a security incident once the security incident is closed.


</td></tr><tr><td>

Security Posture Control

</td><td>

-   Security Posture Control relies on data from service graph connectors that is populated in the CMDB 360 Data \[cmdb\_multisource\_data\] table. This data is populated only when the glide.identification\_engine.multisource\_enabled system property is set to true. You must have the cmdb\_ms\_admin role to modify property values. To set the property, navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**.
-   The labels on the form view for the mitigation control details record associated with vulnerable item records \(VITs\) have been enhanced for more clarity. These updates make the interface more user-friendly by expanding abbreviations on the form view, such as changing "EDR" to "Endpoint Protection."

</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

View annotations for the most recent activity along with a compact email header that includes the subject, sender, and receiver details in the activity stream. Focus on new or unread email messages rather than the entire email conversation.

View or edit the interaction record while drafting an email in a modeless dialog, keeping all relevant information accessible.

-   **[Using Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Leave a chat without ending it for other agents, enabling you to complete your task and exit the chat.

Confirm before closing a chat tab to avoid unintentionally leaving the chat.

Enable multiple agents to add wrap-up codes and comments for a single chat.

-   **[Import queues](https://www.servicenow.com/docs/access?context=import-queues&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Review and update queues imported from a contact center in a post-import page. The post-import page for a queue mirrors the existing post-import pages for skills and wrap-up codes, providing a consistent user experience.

-   **[Interaction Controls Component \(ICC\) call features](https://www.servicenow.com/docs/access?context=interaction-controls-component-icc-call-interaction-features&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Notify agents when a supervisor is coaching or has joined an active call while monitoring agents directly through the CCaaS system.

-   **[CCaaS callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Callback management has been improved to make handling requests easier for agents. The key changes include:

    -   Equip agents to transfer the callback requests before dialing the call, enhancing flexibility in managing customer interactions.
    -   Enable scheduled callbacks, which help customers to choose a preferred callback time in addition to the existing ASAP option.
    -   Facilitate agents to view the list of queues and other agents for easier callback transfers and efficient customer management.
    -   Capture callback reasons more effectively with the expanded Reason for Call field, which includes additional choice values.
-   **[Unified routing of email interactions via CCaaS](https://www.servicenow.com/docs/access?context=using-email-interaction-customer-service-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Email interaction handling has been enhanced to improve efficiency and responsiveness in managing customer communications. The key changes include:

    -   Support external routing of email interactions.
    -   Enable agents to put email interactions on hold while waiting for customer responses.
    -   Notify CCaaS when an interaction is put on hold so that CCaaS can free up the agent's capacity for handling other interactions.
    -   Send automatic email reminders to customers for interactions that are on hold for a configurable period.
    -   Reroute email interactions to available agents when the originally assigned agent is unavailable.
    -   Prevent creating outbound email interactions when emails are sent on top of cases.
-   **[Import queues](https://www.servicenow.com/docs/access?context=import-queues&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

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

-   **[A property to delete a draft of catalog item](https://www.servicenow.com/docs/access?context=save-draft-catalog-item&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Use the property **glide.sc.delete\_draft\_item\_on\_version\_change** to determine whether to delete a saved draft of a catalog item on its modification.

-   **[Dynamic Lookup Choices and Enhanced Table Sourcing](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Lookup questions are now more flexible and user-friendly. You can effortlessly display choices directly from a specific table field, offering similar ease for select box configurations. Additionally, create dynamic dependent lookups where the choices refresh automatically based on the values selected in other fields on the same form, guiding users to more relevant selections.

-   **[Enhanced Sorting Control for Lookup Fields](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Customize the display order in lookup select boxes, look up multiple choice, and list collector fields with the new **ref\_ac\_order\_by** attribute. This attribute enables options to be sorted primarily by a specified data column, and then by their display label, providing a more logical and predictable presentation for users.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Configure help and order of the remedial action parameters](https://www.servicenow.com/docs/access?context=components-installed-with-remediation-fw&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Configure the **Help** and **Order** fields for the remedial action parameters on the Remedial action parameter \[sn\_reacf\_remedial\_action\_parameter\] table if you have the Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\] user role.

-   **[List page enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-incident-list-page-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The list page in SOW has the following enhancements:

    -   The related lists in the **Related records** tab of the SOW record pages, including those within the record pages as well such as Recent Incidents or Assigned Assets, are updated with the record list bundle. This update provides them with the same appearance, functionality, and user experience as the SOW list page.
    -   The related lists in the **Related records** tab of the SOW record pages, including the Multi Record Associator \(MRA\) list, as well as the related lists within the record pages such as Recent Incidents or Assigned Assets, now support the fuzzy count UX page property. You can configure a default value that is applicable to the list for all tables or a value for a specific table such as incident thereby improving the list page performance.
-   **[Dependency view changes for reference fields](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Selecting the dependency view for the following fields in the incident, problem, change, and request records, opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:

    -   Configuration item
    -   Service
    -   Service offering
-   **[Propose a standard change template](https://www.servicenow.com/docs/access?context=propose-standard-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As a user with the itil role, you can create a standard change template proposal from any change record in SOW.

-   **[Service Operations Workspace access for an on-call shift administrator](https://www.servicenow.com/docs/access?context=roles-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Starting in version 8.2, a user with the rota\_admin role can access Teams, Schedules, and Home pages in SOW.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://www.servicenow.com/docs/access?context=javascript-engine-feature-support&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

Use additional scripting features, including Promises and Async await, in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[Stream multipart responses with REST APIs](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Stream multipart responses rather than buffering responses until complete by default with REST APIs that support the multipart/mixed requests, such as the Batch API. The **glide.rest.serialize.disable\_response\_stream\_buffering** system property controls this behavior and applies only to instances configured with Application Delivery Controller, version 2 \(ADCv2\).

-   **[Additional field types supported in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The following field types are now supported for use in a configurable workspace:

    -   **datetime**
    -   **email\_script**
    -   **int**
    -   **integer\_time**
    -   **related\_tags**
    -   **user\_input**
-   **[Vertical layout configuration for radio buttons in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Configurable workspaces now support a vertical layout configuration of radio buttons.

-   **[More dictionary attributes available for selected fields in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

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
-   **[New plugins available for the TinyMCE HTML editor](https://www.servicenow.com/docs/access?context=configuring-the-html-plugins-for-tinymce&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The TinyMCE HTML editor now supports two new plugins in Core UI and configurable workspaces:

    -   The Image Editing \(editimage\) plugin adds a contextual editing toolbar to images in the editor.
    -   The Help plugin \(help\) enables you to check shortcuts and keyboard navigation for accessibility.
-   **[New run types available for scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The following run types are now available for all scheduled job types, enabling flexible scheduling:

    -   **Day and Month in Year**
    -   **Day in Week in Month in Year**
    -   **Week in Month**
The new run types are available in the following standard scheduled job types:

    -   **Scheduled Email of Report**
    -   **Scheduled Entity Generation**
    -   **Scheduled Script Execution**
To enable these new run types in other scheduled job child tables, you must configure your applicable form view to include the fields **Day**, **Month**, and **Year**. For more information, see [Enable run types for scheduled job child tables](https://www.servicenow.com/docs/access?context=customize-run-times-for-scheduled-jobs&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **[New advanced options available for scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The following new advanced options are available when configuring scheduled jobs, offering greater flexibility in job planning, execution, and recurrence:

    -   **Starting**
    -   **Ending**
    -   **Repeat every**
-   **[Export lists to Google Sheets](https://www.servicenow.com/docs/access?context=setup-gsheet-export&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Export your lists to Google Sheets directly from the Export menu.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Get type checking and validation of client-side TypeScript files](https://www.servicenow.com/docs/access?context=ui-development-react&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Full-stack TypeScript applications support type checking and validation of `.ts` and `.tsx` files in the `src/client` directory when building applications.


-   **[Manage dependencies with additional parameters on the dependencies command](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&section=now-sdk-dependencies-command&ft:locale=en-US)**

Control which dependencies and TypeScript definitions to download with additional parameters on the `now-sdk dependencies` command.

-   **[Use additional column types with ServiceNow Fluent](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the following additional types of table columns with ServiceNow Fluent APIs: Password2Column, GuidColumn, JsonColumn, NameValuePairsColumn, UrlColumn, EmailColumn, HTMLColumn, FloatColumn, MultiLineTextColumn, DurationColumn, TimeColumn, FieldListColumn, SlushBucketColumn, TemplateValueColumn, and ApprovalRulesColumn.


-   **[Download TypeScript definitions for script includes used in JavaScript modules](https://www.servicenow.com/docs/access?context=downloading-dependencies-now-sdk&version=zurich&pubname=zurich-application-development&section=download-script-dependencies&ft:locale=en-US)**

Download TypeScript definitions for script includes imported in JavaScript modules from an instance using the `now-sdk dependencies` command.

-   **[Apply a template to an existing application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&section=now-sdk-create-command&ft:locale=en-US)**

Add template files and directories for development in ServiceNow Fluent using the `--template` parameter with the `now-sdk init` command in an existing application.


-   **[Automated Test Framework API supports additional test steps](https://www.servicenow.com/docs/access?context=atf-test-now-ts&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the following test steps with the ServiceNow Fluent Automated Test Framework API.

    -   atf.form.addAttachmentsToForm
    -   atf.form\_SP.addAttachmentsToForm
    -   atf.server.addAttachmentsToExistingRecord
    -   atf.server.runServerSideScript
    -   atf.server.setOutputVariables
-   **[Build command doesn't package build artifacts](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the `now-sdk pack` or `now-sdk install` commands to package build artifacts. The `now-sdk build` command compiles the source files but doesn't package the build artifacts.


</td></tr><tr><td>

Skills Foundation

</td><td>

-   **[Skills Foundation](https://www.servicenow.com/docs/access?context=skills-intelligence&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Skills search is powered by AI Search capability instead of machine learning models. You can configure the skill search to be indexed based on the skill name or description or both. For Pro Plus License \(i.e. LLM Integration\) customers, AI search with RAG configuration is provided to power skill search.

Multilingual skill support is limited to the languages supported by AI Search, which is fewer than the previously supported 23 languages.

Resume parsing is done using Now Assist.

ITSM skills previously stored in the CDS plugin were moved back to the seed data plugin.


-   **[Skills Workspace](https://www.servicenow.com/docs/access?context=skills-intelligence-workspace&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The application name Skills Intelligence Workspace has been changed to Skills Workspace.

Role group skill recommendations will not be readily available unless you load your own ontology data to the industry plugin.

In Skill Harmonization, duplicate skills identification relies on AI search instead of ML models, which will have some quality impact in identifying duplicates.

In Skills Import, two new integration options are added for SAP SuccessFactors and skills and user skills imported go through harmonization pipeline.


-   **[Career tab in Employee Center](https://www.servicenow.com/docs/access?context=manage-skills-profile&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

In the Career tab, the recommended skills source is now derived both from skills that are tagged to activities that employees has been pursuing and from similar user skills.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Publisher optimizations for Microsoft](https://www.servicenow.com/docs/access?context=pub-opt-microsoft&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.

-   **[Publisher optimizations for SAP](https://www.servicenow.com/docs/access?context=pub-opt-sap&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

The Publisher Optimizations dashboard for SAP has been updated with a report on SAP HANA Database monthly peak usage.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Components installed with Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=installed-with-FSC&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Negotiation event table label has been renamed to Sourcing event. This change affects the label only. The underlying table name, \[sn\_shop\_negotiation\_event\], remains unchanged.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Investment type and Investment class fields](https://www.servicenow.com/docs/access?context=planning-item-form&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

The **Investment type** and **Investment class** fields have been deprecated from the Project and Demand planning item tables. These fields are now created at the parent level in the Planning item \[sn\_align\_core\_planning\_item\] table.

-   **[Goal management](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed across the workspace. This change applies to the **Dashboards** and **Goals and targets** tabs on the Goals page, the **Goal**/**Parent goal** reference fields in all applicable tables, and all relevant dashboards.

-   **[Default related list view changes for Stories](https://www.servicenow.com/docs/access?context=create-single-or-multiple-child-items-for-epic-in-eap&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

In the Stories list for an Epic, Feature, or Capability in the Enterprise Agile Planning workspace, the Assignment group and Sprint columns in the default related list view are replaced with the EAP team and Iteration columns.

-   **[Enhancements to tables in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.

</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Assist usage excludes demo data](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Demonstration instances are excluded from the total Assist usage count to improve tracking of Assist consumption.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Now Assist usage measurement is evolving. If your instances are below Zurich Patch 6, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Hidden user-based subscription allocations](https://www.servicenow.com/docs/access?context=subscriptions-overview-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Define network service instance details](https://www.servicenow.com/docs/access?context=create_application_services&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

**xNF Instance** is renamed to **Service Instance**.

-   **[Define network function details](https://www.servicenow.com/docs/access?context=create_business_applications&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

**xNF** is renamed to **Network Function**.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Telecom Discovery via Nokia Altiplano](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

Nokia Altiplano SGC enables you to do the following:

    -   Discover logical inventory for Nokia Altiplano such as logical ports, LAGs, and logical connections.
    -   Enable customers to manage both physical infrastructure and logical network relationships on the ServiceNow AI Platform.
    -   Store logical elements in the CMDB, improving visibility and traceability across the network.
    -   Use the generic Extract, Transform, Load \(ETL\) framework provided by ServiceNow to integrate with Nokia Altiplano, significantly reducing development effort.
-   **[Discrepancy identification](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

Use the enhanced audit and reconciliation logic to do the following:

    -   Detect mismatches in logical elements such as logical ports, LAGs, and connections.
    -   Filter audit results by IP range, device type, or vendor to focus on relevant subsets of data.
    -   Enhance audit performance, usability, and customer satisfaction by reducing unnecessary processing.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Risk areas extended to internal assessments](https://www.servicenow.com/docs/access?context=create-sae-q-template&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Starting with version 21.1.x, if you have the third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_admin\] role, you can now configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace. Risk scores can be aggregated at the engagement level using customizable methods such as max, min, or average, and mapped to risk ratings based on business rules. Risk managers can override system-generated ratings with required justification, enabling expert judgment and helping ensure transparency in risk decisions.

-   **[Smart Assessment Engine advanced plugins](https://www.servicenow.com/docs/access?context=tprm-migrate-asmnt-sae&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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
-   **[Fourth-party assessment support in SAE](https://www.servicenow.com/docs/access?context=tprm-monitor-fourth-parties&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Starting with version 21.1.x, Fourth-party assessments are now supported after you enable the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   ****

Aggregate and analyze the data from internal systems through internal intelligence included in the Investigation Canvas module to help you identify potential threats more effectively.


-   **[Import Intelligence in TISC](https://www.servicenow.com/docs/access?context=importing-threat-intelligence&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Enhanced the Import Intelligence functionality to support direct import of allow list observables.

-   **[Working with Investigation Canvas](https://www.servicenow.com/docs/access?context=tisc-investigation-canvases&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Investigation Canvas feature has been extended to include customized nodes, node relationships, and node legends, as well as the grouping and ungrouping of nodes.

-   **[Investigation canvas and MITRE ATT&amp;CK](https://www.servicenow.com/docs/access?context=investigation-and-mitre&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Navigate and use the MITRE-ATT&amp;CK model within the Investigation Canvas more effectively by taking advantage of enhanced filtering options.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Add events to track components with unsaved changes](https://www.servicenow.com/docs/access?context=dirty-state-event&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use an event to quickly identify modified components.

-   **[Configure alerts to auto-dismiss](https://www.servicenow.com/docs/access?context=uib-configure-alerts&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Enable alerts to auto-dismiss across an experience by configuring all of them in the experience settings or individually through an event.

-   **Use pages across experiences**

Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.

-   **[Use the floating Now Assist panel to streamline your workflow](https://www.servicenow.com/docs/access?context=uib-now-assist-panel&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of UI Builder version 28.2, the fixed Now Assist panel has been replaced with a drag-enabled floating panel improving layout flexibility and workflow visibility.

-   **[Specify your page type in the Create a page wizard](https://www.servicenow.com/docs/access?context=create-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of UI Builder version 28.2, the Create a page wizard now includes a page**Type** dropdown field. This new field helps you to later identify and filter important pages within the Experience view list, especially helpful in large experiences with many pages.

-   **[Explore the newly enhanced Experience view](https://www.servicenow.com/docs/access?context=nav-uib&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of UI Builder version 28.2, the Experience view has improved usability in the following ways:

    -   Pages and their variants appear collapsed by default for a cleaner, more focused view.
    -   Locate pages and variants with ease utilizing the search field.
    -   Search by name, URL, URL type, or variant, and toggle between filters for a cleaner, more intuitive page list.
    -   Pagination is automatically enabled when 10 or more pages are present.

</td></tr><tr><td>

Upgrade Console

</td><td>

-   **[Updated access to Guided upgrade](https://www.servicenow.com/docs/access?context=um-guided-tour-implement&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Apart from the **Guided upgrade** tab option, you can also access Guided upgrade by selecting **Resume upgrade** if there is an ongoing upgrade in the instance.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#section_gsl_nw5_vyb)**

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

-   **[Granular VIT creation for Microsoft TVM recommendations](https://www.servicenow.com/docs/access?context=vr-configure-vi-key&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now configure recommendation as a vulnerability item \(VIT\) key for Microsoft Threat &amp; Vulnerability Management \(TVM\). This enhancement enables each recommendation to generate a separate vulnerable item, offering more granular control for tracking, assigning, and managing remediation efforts, especially when different recommendations require actions from different teams.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.

-   **[Ability to manually cancel Exposure Assessment background jobs](https://www.servicenow.com/docs/access?context=vr-ws-exposure-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Vulnerability Admins and Event Managers can now cancel Exposure Assessment background jobs that were triggered with incorrect parameters or are taking longer than expected. This enhancement reduces downtime by removing the need to wait for the job to complete. Once cancelled, the sub-state is immediately set to User cancelled, and the state updates to Complete after the job is fully terminated; giving you better control and flexibility.

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=vr-max-rows-rel-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Qualys Integration – Detection Splitting](https://www.servicenow.com/docs/access?context=split-qualys-detections&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use the Qualys Host Detection Integration to create a separate VIT for each vulnerability instance based on proof. This improves accuracy in vulnerability tracking and supports clearer team ownership during remediation.

-   **[Activate the Qualys QVS score integration](https://www.servicenow.com/docs/access?context=optional-modifications&version=zurich&pubname=zurich-security-management&section=enable-qualys-qvs-score&ft:locale=en-US)**

Add Qualys-specific risk context to CVEs by importing QVS scores, helping you make more informed prioritization decisions.


</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   **[SAP ECC primary connector](https://www.servicenow.com/docs/access?context=sap-ecc-primary-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

The SAP ECC connector is now certified as a primary connector.

-   **[SAP S/4HANA primary connector](https://www.servicenow.com/docs/access?context=sap-s4hana-primary-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

The SAP S/4HANA connector is now certified as a primary connector.

-   **[Primary connectors in preview](https://www.servicenow.com/docs/access?context=primary-connectors-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Primary connectors that are still being enhanced to include all planned functionality are now identified as in preview. These connectors are fully supported by ServiceNow®.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **Additional system property to specify how many records are retrieved**

The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Zero Copy Connector for ERP Enterprise Data Foundation data product](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Quote to Cash data product](https://www.servicenow.com/docs/access?context=erp-canvas-sales-order-content-pack&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Source to Settle data product](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)

