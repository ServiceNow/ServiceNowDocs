---
title: Combined API release notes for upgrades from Zurich to Brazil
description: Consolidated page of all release notes for API from Zurich to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-brazil/brazil-zurich-api-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Zurich to Brazil

Consolidated page of all release notes for API from Zurich to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideCurrencyCode - Scoped, Global](https://www.servicenow.com/docs/access?context=GlideCurrencyCodeBothAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getCurrencyCode\(\)
-   getNumericCurrencyCode\(\)

</td></tr><tr><td>

[GlideCurrencySymbol - Scoped, Global](https://www.servicenow.com/docs/access?context=GlideCurrencySymbolBothAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getCurrencySymbol\(\)
-   getSortedActiveCurrencySymbols\(\)

</td></tr><tr><td>

[GlideQueryCondition - Scoped](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Scoped](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addSystemEncodedQuery\(\)
-   addSystemQuery\(\)
-   addSystemOrderBy\(\)
-   addSystemOrderByDesc\(\)
-   addUserEncodedQuery\(\)
-   addUserQuery\(\)
-   addUserOrderBy\(\)
-   addUserOrderByDesc\(\)

</td></tr><tr><td>

[GlideSysAttachment - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSysAttachmentScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addAttribute\(\)
-   addMultipleAttributes\(\)
-   deleteAllAttributes\(\)
-   deleteAttribute\(\)
-   fetchAllAttributes\(\)
-   fetchAttribute\(\)
-   updateAllAttributes\(\)
-   updateAttribute\(\)

</td></tr><tr><td>

[GlideSystem - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addSuccessMessage\(\)
-   addModerateMessage\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New method getNamespaceName\(\).

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&family=zurich&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New methods:

-   getDynamicNamespace\(\)
-   setDynamicNamespace\(\)

</td></tr><tr><td>

[GlideDynamicNamespace - Global](https://www.servicenow.com/docs/access?context=GlideDynamicNamespaceAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getName\(\)
-   isActive\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideQueryCondition - Global](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addSystemEncodedQuery\(\)
-   addSystemQuery\(\)
-   addSystemOrderBy\(\)
-   addSystemOrderByDesc\(\)
-   addUserEncodedQuery\(\)
-   addUserQuery\(\)
-   addUserOrderBy\(\)
-   addUserOrderByDesc\(\)

</td></tr><tr><td>

[GlideSysAttachment - Global](https://www.servicenow.com/docs/access?context=GlideSysAttachmentGlobalAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addAttribute\(\)
-   addMultipleAttributes\(\)
-   deleteAllAttributes\(\)
-   deleteAttribute\(\)
-   fetchAllAttributes\(\)
-   fetchAttribute\(\)
-   updateAllAttributes\(\)
-   updateAttribute\(\)

</td></tr><tr><td>

[GlideSystem - Global](https://www.servicenow.com/docs/access?context=c_GlideSystemAPI&family=zurich&ft:locale=en-US)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)

</td></tr><tr><td>

[Message - Global](https://www.servicenow.com/docs/access?context=sn_i18n.messageAPI&family=zurich&ft:locale=en-US)

</td><td>

Retrieves localized messages from the Message \[sys\_ui\_message\] table. It supports internationalization \(i18n\) by dynamically fetching messages based on the user's session language or a specified language parameter.-   getMessage\(\)
-   getMessageLang\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://www.servicenow.com/docs/access?context=c_GlideFormAPI&family=zurich&ft:locale=en-US)

</td><td>

-   addChoice\(\)
-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)
-   clearChoices\(\)
-   disableChoice\(\)
-   enableChoice\(\)
-   getAnnotationByName\(\)
-   getAnnotations\(\)
-   getChoice\(\)
-   getOptions\(\)
-   hideAnnotation\(\)
-   hideRelatedLinks\(\)
-   hideTemplateBar\(\)
-   removeChoice\(\)
-   setChoiceLabel\(\)
-   setRelatedLinksDisplay\(\)
-   showAnnotation\(\)
-   showRelatedLinks\(\)
-   showTemplateBar\(\)
-   toggleAnnotations\(\)

</td></tr><tr><td>

[GlideModal \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GModClientAPINX&family=zurich&ft:locale=en-US)

</td><td>

-   destroy\(\)
-   get\(\)
-   getID\(\)
-   getPreference\(\)
-   getPreferences\(\)
-   renderWithContent\(Object\)
-   renderWithContent\(String\)
-   setDialog\(\)
-   setPreference\(\)
-   setTitle\(\)
-   type\(\)

</td></tr><tr><td>

[GlideNavigation \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideNavigationClientAPINX&family=zurich&ft:locale=en-US)

</td><td>

refreshNavigator\(\)

</td></tr><tr><td>

[StopWatch \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=StopWatchAPINX&family=zurich&ft:locale=en-US)

</td><td>

-   StopWatch\(\)
-   getTime\(\)
-   restart\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideFormAPINX&family=zurich&ft:locale=en-US)

</td><td>

-   addChoice\(\)
-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)
-   clearChoices\(\)
-   disableChoice\(\)
-   enableChoice\(\)
-   getAnnotationByName\(\)
-   getAnnotations\(\)
-   getChoice\(\)
-   getOptions\(\)
-   hideAnnotation\(\)
-   removeChoice\(\)
-   setChoiceLabel\(\)
-   showAnnotation\(\)
-   toggleAnnotations\(\)

</td></tr><tr><td>

[GlideUser \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideUserAPINX&family=zurich&ft:locale=en-US)

</td><td>

getRoles\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Conversation Member API](https://www.servicenow.com/docs/access?context=conversation-member-api&family=zurich&ft:locale=en-US)

</td><td>

-   PUT now/conversation/member/\{user\_id\}/drop
-   PUT now/conversation/member/\{user\_id\}/update

</td></tr><tr><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

[CSM Pricing API](https://www.servicenow.com/docs/access?context=csm-pricing-api&family=zurich&ft:locale=en-US)

</td><td>

-   POST /api/sn\_csm\_pricing/pricingengine/computePrice
-   DELETE /api/sn\_csm\_pricing/pricingengine/pricing\_context/\{pricing\_context\_id\}

</td></tr></tbody>
</table>

</td></tr><tr><td>

Australia

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&family=australia&ft:locale=en-US)

</td><td>

Methods:

-   getCopyApi\(\)
-   skipAttributes\(\)
-   skipChoiceOverrides\(\)
-   skipChoiceSets\(\)
-   getTransactionId\(\)
-   runAsync\(\)

 Extension points:

-   getCopyName\(\)
-   shouldCopy\(\)
-   verifyCopyOperation\(\)

</td></tr><tr><td>

[GlideAggregate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideAggregateScopedAPI&family=australia&ft:locale=en-US)

</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>

[GlideDate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideDateScopedAPI&family=australia&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideTime - Scoped](https://www.servicenow.com/docs/access?context=c_GlideTimeScopedAPI&family=australia&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   getDisplayValueLang\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)

</td></tr><tr><td>

[GlideElementDescriptor - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&family=australia&ft:locale=en-US)

</td><td>

[GlideElementDescriptor - isEncrypted\(\)](https://www.servicenow.com/docs/access?context=SGED-isEncrypted&family=australia&ft:locale=en-US)

</td></tr></tbody>
</table><table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Product Catalog Management

</td><td>

v19.2.0

</td><td>

2026-08

</td><td>

[CatalogSearchAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-scoped_global&family=australia&ft:locale=en-US)

</td><td>

The new getEligibleCatalogCategoryHierarchy\(\) method lets you retrieve the complete product catalog-category hierarchy for a given context \(customer, currency, pricing rules, etc.\). The API automatically applies eligibility rules to filter out ineligible catalogs and categories, ensuring that customers see only the offerings they qualify for.**Note:** The REST version of this endpoint is [Product Catalog Search - POST /api/sn\_prd\_pm/v1/catalog/eligible-catalog-category-hierarchy](https://www.servicenow.com/docs/access?context=prod_catalog_search-POST-hierarchy&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Product Catalog Management

</td><td>

v20.0

</td><td>

2026-07

</td><td>

[CatalogSearchAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-scoped_global&family=australia&ft:locale=en-US)

</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named to `CatalogSearch` Server API, the new `CatalogSearchAPI` is a higher-level wrapper specifically for the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The [Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US) REST API wraps this Server API.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>

[ConsolidationService - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsolidationServiceAPI&family=australia&ft:locale=en-US)

</td><td>

-   canConsolidateEntity\(\)
-   canConsolidateJSONs\(\)
-   canMergeEntity\(\)
-   consolidate\(\)
-   enableConsolidation\(\)
-   getHashConfig\(\)
-   getPrimary\(\)
-   overrideAttributeValues\(\)
-   postHierarchyConsolidation\(\)
-   preProcess\(\)

</td></tr><tr><td>

MCP Client

</td><td>

v1.0.1

</td><td>

2026-05

</td><td>

[MCPClient - Scoped](https://www.servicenow.com/docs/access?context=MCPClientAPI&family=australia&ft:locale=en-US)

</td><td>

-   MCPClient\(\)
-   getServers\(\)
-   getToolInfo\(\)
-   invokeTool\(\)
-   listTools\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&family=australia&ft:locale=en-US)

</td><td>

Methods:

-   getCopyApi\(\)
-   skipAttributes\(\)
-   skipChoiceOverrides\(\)
-   skipChoiceSets\(\)
-   getTransactionId\(\)
-   runAsync\(\)

 Extension points:

-   getCopyName\(\)
-   shouldCopy\(\)
-   verifyCopyOperation\(\)

</td></tr><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&family=australia&ft:locale=en-US)

</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&family=australia&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideElement - Global](https://www.servicenow.com/docs/access?context=c_GlideElementAPI&family=australia&ft:locale=en-US)

</td><td>

getDynamicNamespace\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&family=australia&ft:locale=en-US)

</td><td>

-   getDynamicAttributePathsInSchema\(\)
-   getDynamicAttributePathsInStore\(\)
-   getDynamicNamespaceName\(\)

</td></tr><tr><td>

[MIDHermesProducer - Global](https://www.servicenow.com/docs/access?context=MIDHermesProducerAPI&family=australia&ft:locale=en-US)

</td><td>

-   MIDHermesProducer\(\)
-   send\(\)

</td></tr><tr><td>

[GlideElementDescriptor - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&family=australia&ft:locale=en-US)

</td><td>

[GlideElementDescriptor - isEncrypted\(\)](https://www.servicenow.com/docs/access?context=SGED-isEncrypted&family=australia&ft:locale=en-US)

</td></tr></tbody>
</table><table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Automated Test Framework

</td><td>

v3.1

</td><td>

2026-08

</td><td>

[Cloud Runner TestRunnerApi – Scoped, Global](https://www.servicenow.com/docs/access?context=cloudrnr-TestRunnerAPI-scoped&family=australia&ft:locale=en-US)

</td><td>

Three new methods enable asynchronous test job management without requiring `sn_boq` record creation:-   cancelJobByTracker
-   progressFromTracker
-   startJob

Use these methods when you start a test run with `startJobAsync` and only have the `rootTrackerId`; no need to poll for a `sn_boq` record.

</td></tr><tr><td>

Product Catalog Management

</td><td>

v20.0

</td><td>

2026-07

</td><td>

[CatalogSearchAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-scoped_global&family=australia&ft:locale=en-US)

</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named, to `CatalogSearch`, the new `CatalogSearchAPI` is used within the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The [Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US) REST API wraps this Server API.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>

[ConsolidationService - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsolidationServiceAPI&family=australia&ft:locale=en-US)

</td><td>

-   canConsolidateEntity\(\)
-   canConsolidateJSONs\(\)
-   canMergeEntity\(\)
-   consolidate\(\)
-   enableConsolidation\(\)
-   getHashConfig\(\)
-   getPrimary\(\)
-   overrideAttributeValues\(\)
-   postHierarchyConsolidation\(\)
-   preProcess\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&family=australia&ft:locale=en-US)

</td><td>

-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes
-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachments/\{attachment\_sys\_id\}/attributes
-   PATCH /now/attachment/\{sys\_id\}
-   POST /now/attachment/\{attachment\_sys\_id\}/attributes
-   PUT /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}

</td></tr><tr><td>

[Help Request API](https://www.servicenow.com/docs/access?context=help-request-api&family=australia&ft:locale=en-US)

</td><td>

POST /now/helprequest/action/create\_or\_update

</td></tr><tr><td>

[ATF Code Coverage API](https://www.servicenow.com/docs/access?context=atf-code-coverage-api&family=australia&ft:locale=en-US)

</td><td>

-   POST /now/atf/code\_coverage/all
-   POST /now/atf/code\_coverage/by\_line\_number
-   POST /now/atf/code\_coverage/by\_script\_id

</td></tr><tr><td>

[Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&family=australia&ft:locale=en-US)

</td><td>

-   POST /api/sn\_csm\_pricing/\{api\_version\}/pricingengine/computePrice
-   DELETE /api/sn\_csm\_pricing/pricingengine/pricing\_context/\{pricing\_context\_id\}

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://www.servicenow.com/docs/access?context=warranty-claims-SOAP-API&family=australia&ft:locale=en-US)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

</td></tr><tr><td>

Brazil

</td><td>

-   ****

<table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API type

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Offering Qualification API](https://www.servicenow.com/docs/access?context=product-offering-qualification-api&family=brazil&ft:locale=en-US)

</td><td>

-   POST /queryProductOfferingQualification
-   POST /checkProductOfferingQualification


</td></tr></tbody>
</table>


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing API features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideSysAttachment - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSysAttachmentScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngine - Scoped](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[ProducerV2 - Scoped](https://www.servicenow.com/docs/access?context=ProducerV2ScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

send\(\) - Added a return value and error handling.

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&family=zurich&ft:locale=en-US)

</td><td>

setHttpMethod\(\) - Added support for HEAD method calls via the **method** parameter.

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&family=zurich&ft:locale=en-US)

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

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US)

</td><td>

Remove support for groups in Dynamic Schema. -   getGroupName\(\)
-   getName\(\)
-   getPath\(\)
-   getType\(\)
-   isTransient\(\)

Remove getSysId\(\).

Remove GlideTransientDynamicAttribute API documentation because GlideDynamicAttribute and GlideTransientDynamicAttribute APIs provide the same solution.

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&family=zurich&ft:locale=en-US)

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

[GlideSysAttachment - Global](https://www.servicenow.com/docs/access?context=GlideSysAttachmentGlobalAPI&family=zurich&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngineScriptableApi - Global](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&family=zurich&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&family=zurich&ft:locale=en-US)

</td><td>

setHttpMethod\(\) - Added support for HEAD method calls via the **method** parameter.

</td></tr></tbody>
</table>

</td></tr><tr><td>

Australia

</td><td>

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

</td></tr><tr><td>

Brazil

</td><td>

-   ****

<table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API type

</th><th>

API

</th><th>

Methods/endpoints

</th></tr></thead><tbody><tr><td>

Workplace Calendar Synchronization

</td><td>

3.4.16

</td><td>

REST

</td><td>

[WSD Recurring Reservation API](https://www.servicenow.com/docs/access?context=wsd_recur_reserv-api&family=brazil&ft:locale=en-US)

</td><td>

POST /create\_series: The recurringPattern parameter now uses RFC 5545 iCalendar format \(freq, dtstart, interval, byweekday, tzid, etc.\) for better timezone handling and standards compliance. **Note:** Legacy format patterns \(using repeats, options.\*, and startDate\) remain supported and continue to work without changes.

</td></tr><tr><td>

Interaction Controls Component

</td><td>

3.0.1

</td><td>

Client

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=brazil&ft:locale=en-US)

</td><td>

-   setICContext\(\): Supports supervisor monitoring controls \(coaching, monitoring, barging\), callback transfer enhancements with directTarget support, and clarified conditional logic for callback context timing.
-   subscribe\(\): Supports five new callback-related sub-actions \(callbackLeaveAndTransfer, getSearchTarget, getMoreInfo, callbackTransferInitiated, cancelCallbackTransfer\) and the openframe\_icc\_record\_opened event for manager role interaction tracking.

</td></tr><tr><td>

Product Catalog Management Core application

</td><td>

20.0.2

</td><td>

REST

</td><td>

[Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=brazil&ft:locale=en-US)

</td><td>

The POST /search endpoint now returns the **productOfferingFamily** field, which identifies the product offering family that each offering belongs to.

</td></tr><tr><td>

Product Catalog Management Core application

</td><td>

20.0.2

</td><td>

Server

</td><td>

[CatalogSearchAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-scoped_global&family=brazil&ft:locale=en-US)

</td><td>

The getCatalogData\(\) now returns the `productOfferingFamily` field, which identifies the product offering family that each offering belongs to.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=brazil&ft:locale=en-US)

</td><td>

PATCH /productOrder/\{id\}: -   Now supports a `changeType=nonProduct` parameter to update order and line item administrative details without triggering product change workflows or state transitions.
-   Now accepts either the system ID \(`sys_id`\) or external ID \(`external_id`\) in the `productOrderItem.id` field, reducing the need for additional lookups when updating line items.
-   Supports associating payment profiles, billing accounts, and related parties \(Account, Contact, Location, and Consumer\) with product orders. This allows clients to link existing records or create new ones inline during order placement for streamlined end-to-end order workflows.
GET/LIST endpoints now support the following query parameters: `Account`, `Contact and Consumer(Related Party)`, `externalID`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=brazil&ft:locale=en-US)

</td><td>

GET/LIST endpoints now support the following query parameters: `Account`, `Contact and Consumer(Related Party)`, `externalID`, `expectedStartDate`, `CompletionDate`, `requestedStartDate`, `requestedCompletionDate`, `expectedCompletionDate`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=brazil&ft:locale=en-US)

</td><td>

GET/LIST endpoints now support the following query parameters: `Account`, `Contact` and `Consumer`\(Related Party\), `billingAccount`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=brazil&ft:locale=en-US)

</td><td>

GET/LIST endpoints now support the following query parameters: `externalID`, `isSellable`

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Service Test Management Open API](https://www.servicenow.com/docs/access?context=service-test-management-api&family=brazil&ft:locale=en-US)

</td><td>

All GET and POST endpoints responses return `id` and `externalId` as distinct fields on ServiceTest and ServiceTestSpecification resources. The `id` field returns the record's `sys_id`, and `externalId` returns the value of the `external_id` column when one is set. Existing query resolution behavior is unchanged, so requests that filter on an external identifier continue to work.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=brazil&ft:locale=en-US)

</td><td>

GET/LIST endpoints: Supports the Accept-Language request header on GET and LIST operations for retrieving translated field values, and filtering by translated name on LIST operations.

</td></tr></tbody>
</table>


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some API features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some API features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   The GlideEncrypter API no longer supports Triple Data Encryption Standard \(3DES\) due to updated [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) guidelines.
    -   For existing instances that upgrade to the Zurich release, the GlideEncrypter API is available for use but has been updated to automatically use the Key Management Framework algorithm. See [GlideEncrypter - Global \(deprecated\)](https://www.servicenow.com/docs/access?context=GlideEncrypterAPI&family=zurich&ft:locale=en-US) for more information on how to continue calling this API.
    -   For all new instances created starting with the Zurich release, the GlideEncrypter API is no longer supported. Directly use the [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&family=zurich&ft:locale=en-US) instead for all cryptography operations.
-   Dynamic groups have been removed from dynamic schema in Core Platform. For dynamic attributes defined with an associated dynamic attribute group before the Zurich release, the [GlideDynamicAttribute](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US) getGroupName\(\) method originally designed for dynamic attribute groups continues to work for backwards compatibility.

The getGroupName\(\) method returns null for migrated attributes and newly created attributes.

Customers are urged to migrate to the current [Dynamic Attribute](https://www.servicenow.com/docs/access?context=working-with-dynamic-schema&family=zurich&ft:locale=en-US) definitions to take advantage of future improvements in features and functionality. For migration details, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.


 -   For existing instances that upgrade to the Zurich release, the GlideEncrypter API is available for use but has been updated to automatically use the Key Management Framework algorithm. See [GlideEncrypter - Global \(deprecated\)](https://www.servicenow.com/docs/access?context=GlideEncrypterAPI&family=zurich&ft:locale=en-US) for more information on how to continue calling this API.
-   For all new instances created starting with the Zurich release, the GlideEncrypter API is no longer supported. Directly use the [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&family=zurich&ft:locale=en-US) instead for all cryptography operations.

</td></tr><tr><td>

Australia

</td><td>

-   NowAnalyticsService and NowAnalyticsServiceDelegate have been removed from Mobile SDK - iOS.
-   NowAnalyticsSDK has been removed from Mobile SDK - Android.

 -   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

The following APIs are available by default:

    -   Identification and Reconciliation
    -   IdentificationEngine
    -   IdentificationEngineScriptableApi
    -   GlideDynamicAttribute
    -   GlideDynamicAttributeStore
    -   GlideDynamicNamespace
    -   GlideCurrencyCode
    -   GlideCurrencySymbol
    -   GlideForm \(Next Experience\)
    -   GlideModal \(Next Experience\)
    -   GlideNavigation \(Next Experience\)
    -   GlideQueryCondition
    -   GlideRecord
    -   GlideSysAttachment
    -   GlideUser\(Next Experience\)
    -   StopWatch \(Next Experience\)
The following APIs require plugin activation:

    -   ProducerV2 requires the ServiceNow Stream Connect Installer plugin \(com.glide.hub.stream\_connect.installer\).
    -   Product Order Open API requires the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin.
    -   Service Order Open API requires the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin.
    -   The Omnichannel Callback API requires the Omnichannel Callback \(omnichannel\_callback plugin\) plugin.
    -   Party Management Open API requires the Telecommunications Open APIs \(sn\_tmf\_api\) and Customer Service Management \(com.sn\_customerservice\) plugins.
    -   The SegmentHandle, SegmentHandler, and sn\_erp\_integration API APIs require the Zero Copy Connector for ERP \(com.sn\_erp\_integration\) plugin.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

The following APIs are available by default:

    -   ATF Code Coverage API
    -   Attachment API
    -   GlideAggregate
    -   GlideDate
    -   GlideTime
    -   GlideElement
    -   GlideElementDescriptor
    -   GlideElementDynamicAttributeStore
    -   GlideForm
    -   GlideForm\(Next Experience\)
The following APIs require plugin activation:

    -   CopyDynamicSchemaAPI API requires the Dynamic Schema Support \(com.glide.dynamic\_schema\) plugin.
    -   Help Request API requires the Interactions Management \(com.glide.interaction\) plugin.
    -   MIDHermesProducer requires the MID Hermes API \(com.glide.mid.hermes\_api\) plugin.
    -   Party Management Open API requires the Customer Service Base Entities \(com.snc.cs\_base\) plugin.
    -   Wrap Up API requires the requires the Interactions Management \(com.glide.interaction.awa\) plugin.
    -   WSD Presence API requires the Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin.
    -   WSD Unified Search API requires the Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin.
    -   WSD User API requires the Workplace Service Delivery Concierge \(com.sn\_wsd\_concierge\), Workplace Service Delivery Core \(com.sn\_wsd\_core\), and Workplace Service Delivery Reservation \(com.sn\_wsd\_rsv\) plugins.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for API, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

 See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

 See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-zurich-brazil/rn-combined-intro.md)

