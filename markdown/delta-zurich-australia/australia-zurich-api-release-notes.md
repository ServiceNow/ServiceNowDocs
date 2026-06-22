---
title: Combined API release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for API from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-api-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for API from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for API.

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
</table><table><thead><tr><th>

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

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2026-02

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

</td><td>

Added new endpoints, /get and /close, for retrieving and closing a given callback record. The third endpoint, /actions, allows you to perform create, update, close, and cancel operations for a callback in an external, third-party system with routing capabilities.

-   PATCH api/sn\_omichannel\_callback/get
-   POST api/sn\_omni\_callback/actions
-   POST api/sn\_omni\_callback/callback/close

</td></tr><tr><td>

Contact Center Integration Core

</td><td>

1.5.0

</td><td>

2026-01

</td><td>

[External ID Mapping API](https://www.servicenow.com/docs/access?context=external-id-mapping-api&family=zurich&ft:locale=en-US)

</td><td>

-   GET /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}
-   PUT /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}

</td></tr><tr><td>

Digital Product Release

</td><td>

2.3.0

</td><td>

2025-12

</td><td>

[Digital Product Release API](https://www.servicenow.com/docs/access?context=digital-product-release-api&family=zurich&ft:locale=en-US)

</td><td>

-   GET /sn\_dpr/digital\_product\_release/bundle/\{sysId\}
-   GET /sn\_dpr/digital\_product\_release/releases/\{releaseId\}/policies/status
-   POST /sn\_dpr/digital\_product\_release/product\_enhancement
-   POST /sn\_dpr/digital\_product\_release/release
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/key\_date
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/policies/run
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/related\_task
-   POST /sn\_dpr/digital\_product\_release/release\_calendar
-   POST /sn\_dpr/digital\_product\_release/release\_id/\{releaseId\}/complete\_phase
-   POST /sn\_dpr/digital\_product\_release/release\_target
-   PUT /sn\_dpr/digital\_product\_release/release/\{sysId\}/retarget

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC TAXII Server API](https://www.servicenow.com/docs/access?context=taxii-server-api&family=zurich&ft:locale=en-US)

</td><td>

-   GET /sn\_sec\_tisc/taxii\_server/taxii2
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/manifest
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}/versions

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&family=zurich&ft:locale=en-US)

</td><td>

New API for managing parties with a relationship to the enterprise. Supports the following methods:

-   DELETE /api/sn\_tmf\_api/v1/party/individual/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/individual/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/individual
-   GET/api/ sn\_tmf\_api/v1/party/organization/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/organization
-   PATCH/api/sn\_tmf\_api/v1/party/individual/\{id\}
-   PATCH /api/sn\_tmf\_api/v1/party/organization/\{id\}
-   POST /api/sn\_tmf\_api/v1/party/individual
-   POST /api/sn\_tmf\_api/v1/party/organization

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=zurich&ft:locale=en-US)

</td><td>

-   DELETE /sn\_prd\_invt/order/product/\{id\}
-   PATCH /sn\_prd\_invt/order/product/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&family=zurich&ft:locale=en-US)

</td><td>

Supports new methods for service offerings and service candidate entity:-   DELETE /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory
-   GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   PATCH /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   POST /api/sn\_tmf\_api/catalogmanagement/serviceCategory

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC Intel Exchange API](https://www.servicenow.com/docs/access?context=tisc-intel-ex-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/tisc\_intel\_sharing\_api/post\_intel

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC RPZ API](https://www.servicenow.com/docs/access?context=tisc-rpz-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/rpz\_export

</td></tr><tr><td>

Network Inventory Advanced

</td><td>

10.0

</td><td>

2025-08

</td><td>

[DCIM Metric Data Feed API](https://www.servicenow.com/docs/access?context=dcim-metric-data-feed-api&family=zurich&ft:locale=en-US)

</td><td>

POST /api/sn\_ni\_adv/dcim/feed/\{vendorname\}

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.2

</td><td>

2025-08

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

Quote Management

</td><td>

6.0.1

</td><td>

2025-08

</td><td>

[Quote Management API](https://www.servicenow.com/docs/access?context=quote-management-api&family=zurich&ft:locale=en-US)

</td><td>

-   DELETE /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   GET /sn\_tmf\_api/quote\_management\_api/quote
-   GET /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   PATCH /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   POST /sn\_tmf\_api/quote\_management\_api/quote

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Work Order Management API](https://www.servicenow.com/docs/access?context=work-order-mgmt-api&family=zurich&ft:locale=en-US)

</td><td>

-   CANCEL /sn\_tmf\_api/work\_order\_management\_api/cancelWorkOrder
-   GET /sn\_tmf\_api/work\_order\_management\_api/workordermanagement
-   GET /sn\_tmf\_api/work\_order\_management\_api/workorder/\{id\}
-   PATCH /sn\_tmf\_api/work\_order\_management\_api/workOrder/\{id\}
-   POST /sn\_tmf\_api/work\_order\_management\_api/workOrder

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

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

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

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

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
</table><table><thead><tr><th>

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

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>

[WSD Presence API](https://www.servicenow.com/docs/access?context=wsd_presence-api&family=australia&ft:locale=en-US)

</td><td>

-   DELETE /\{collaborator\_id\}
-   DELETE /exception
-   GET /collaborator
-   GET /exception
-   GET /presence
-   GET /routine
-   PATCH /routine
-   POST /collaborator
-   POST /exception
-   POST /routine
-   PUT /exception

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>

[WSD User API](https://www.servicenow.com/docs/access?context=wsd_user-api&family=australia&ft:locale=en-US)

</td><td>

GET /context

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>

[WSD Unified Search API](https://www.servicenow.com/docs/access?context=wsd_unified-search-api&family=australia&ft:locale=en-US)

</td><td>

-   POST /users\_and\_locations
-   GET /current\_location

</td></tr><tr><td>

Synthetic monitoring

</td><td>

1.5.1

</td><td>

2026-03

</td><td>

[SyntheticsAsyncBulkCreate API](https://www.servicenow.com/docs/access?context=synth-async-api&family=australia&ft:locale=en-US)

</td><td>

-   GET /synthetics\_async\_bulk\_create/\{job\_id\}
-   POST /synthetics\_async\_bulk\_create

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://www.servicenow.com/docs/access?context=warranty-claims-SOAP-API&family=australia&ft:locale=en-US)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing API features.

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

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=zurich&ft:locale=en-US)

</td><td>

createInstance\(\) now supports the **allowedContextTypes** parameter, enabling partial synchronization of updates or deletions for selected Related Parties back to the originating Opportunity. Previously, partial synchronization behavior was limited to quote line items only.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

1.6

</td><td>

2025-12

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=zurich&ft:locale=en-US)

</td><td>

To allow more complex business needs, getPrimitivesEPService\(\) supports the new **context.entityConfigId** parameter, which invokes createInstance\(\) script without any defined mapping using only the entity's configuration ID.

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
</table><table><thead><tr><th>

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

</td><td>

When submitting a change payload with a new or updated service location \(via **productOrderItem.product.place.id**\), the request is now processed as a move order. This means that the product order remains the same but the service is fulfilled in the new designated location.-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](https://www.servicenow.com/docs/access?context=tmf_prod_order-PATCH-ord-productOrder-id&family=zurich&ft:locale=en-US)
-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}](https://www.servicenow.com/docs/access?context=tmf_prod_order-PATCH-productorder-id&family=zurich&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://www.servicenow.com/docs/access?context=tmf_prod_order-POST-ord-productOrder&family=zurich&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder](https://www.servicenow.com/docs/access?context=tmf_prod_order-POST-productOrder&family=zurich&ft:locale=en-US)

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2025-12

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

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

[Trouble Ticket Open API](https://www.servicenow.com/docs/access?context=trouble-ticket-open-api&family=zurich&ft:locale=en-US)

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

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=zurich&ft:locale=en-US)

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

[Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&family=zurich&ft:locale=en-US)

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

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

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=zurich&ft:locale=en-US)

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

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/threat\_intel\_data/observables now supports filtering observables on tags and taxonomies.

</td></tr><tr><td>

Accounts Payable Invoice Processing

</td><td>

v9.5.17

</td><td>

2025-08

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&family=zurich&ft:locale=en-US)

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

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=zurich&ft:locale=en-US)

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

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=zurich&ft:locale=en-US)

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

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=zurich&ft:locale=en-US)

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

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

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

[Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&family=zurich&ft:locale=en-US)

</td><td>

New options for the **action** request body parameter with corresponding examples.POST /sn\_va\_as\_service/bot/integration

</td></tr></tbody>
</table>

</td></tr><tr><td>

Australia

</td><td>

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some API features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some API features or functionality were deprecated.

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


</td></tr><tr><td>

Australia

</td><td>

-   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

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
-   GlideForm \(Next Experience\)

 The following APIs require plugin activation:

-   CopyDynamicSchemaAPI API requires the Dynamic Schema Support \(com.glide.dynamic\_schema\) plugin.
-   Help Request API requires the Interactions Management \(com.glide.interaction\) plugin.
-   MIDHermesProducer requires the MID Hermes API \(com.glide.mid.hermes\_api\) plugin.
-   Party Management Open API requires the Customer Service Base Entities \(com.snc.cs\_base\) plugin.
-   Wrap Up API requires the requires the Interactions Management \(com.glide.interaction.awa\) plugin.
-   WSD Presence API requires the Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin.
-   WSD Unified Search API requires the Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin.
-   WSD User API requires the Workplace Service Delivery Concierge \(com.sn\_wsd\_concierge\), Workplace Service Delivery Core \(com.sn\_wsd\_core\), and Workplace Service Delivery Reservation \(com.sn\_wsd\_rsv\) plugins.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

