---
title: Combined API release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for API from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-api-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 20
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for API from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Australia

</td><td>

<table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

Module

</th><th>

Types

</th></tr></thead><tbody><tr><td>

Mobile SDK Libraries - Android

</td><td>

2.22.0

</td><td>

2026-06

</td><td>

NowVoice

</td><td>

-   [NowVoiceCallbacks interface - Android](https://www.servicenow.com/docs/access?context=NowVoiceCallbacksAndroidInt&family=australia&ft:locale=en-US)
-   [NowVoiceEndpoint class - Android](https://www.servicenow.com/docs/access?context=NowVoiceEndpointAndroidClass&family=australia&ft:locale=en-US)
-   [NowVoiceSDK object - Android](https://www.servicenow.com/docs/access?context=NowVoiceSDKAndroidAPI&family=australia&ft:locale=en-US)
-   [NowVoiceService class - Android](https://www.servicenow.com/docs/access?context=NowVoiceServiceAndroidAPI&family=australia&ft:locale=en-US)
-   [NowVoiceTheme interface - Android](https://www.servicenow.com/docs/access?context=NowVoiceThemeAndroidInterface&family=australia&ft:locale=en-US)
-   [NowVoiceThemeDark class - Android](https://www.servicenow.com/docs/access?context=NowVoiceThemeDarkAndroidClass&family=australia&ft:locale=en-US)
-   [NowVoiceUiConfiguration class - Android](https://www.servicenow.com/docs/access?context=NVoiceUiConfigAndroidClass&family=australia&ft:locale=en-US)
-   [TranscriptMessage class - Android](https://www.servicenow.com/docs/access?context=TranscriptMsgAndroidClass&family=australia&ft:locale=en-US)

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.22.0

</td><td>

2026-06

</td><td>

NowVoice

</td><td>

-   [NowVoice API - iOS](https://www.servicenow.com/docs/access?context=NowVoiceiOSAPI&family=australia&ft:locale=en-US)
-   [NowVoiceCallbacks structure - iOS](https://www.servicenow.com/docs/access?context=NowVoiceCallbacksiOSStruct&family=australia&ft:locale=en-US)
-   [NowVoiceDefaultTheme structure - iOS](https://www.servicenow.com/docs/access?context=NVoiceDefThemeiOSStruct&family=australia&ft:locale=en-US)
-   [NowVoiceEndpoint structure - iOS](https://www.servicenow.com/docs/access?context=NowVoiceEndpointiOSStruct&family=australia&ft:locale=en-US)
-   [NowVoiceService class - iOS](https://www.servicenow.com/docs/access?context=NowVoiceServiceiOSAPI&family=australia&ft:locale=en-US)
-   [NowVoiceThemeable protocol - iOS](https://www.servicenow.com/docs/access?context=NVoiceThemeableiOSProtocol&family=australia&ft:locale=en-US)
-   [NowVoiceTranscriptMessage typealias - iOS](https://www.servicenow.com/docs/access?context=NVoiceTrnstMsgiOSta&family=australia&ft:locale=en-US)
-   [NowVoiceUIConfiguration structure - iOS](https://www.servicenow.com/docs/access?context=NowVoiceUIConfigiOSStruct&family=australia&ft:locale=en-US)

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

Product Catalog Management

</td><td>

v19.2.0

</td><td>

2026-08

</td><td>

[Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US)

</td><td>

POST /eligible-catalog-category-hierarchy is a new endpoint that retrieves the complete product catalog-category hierarchy for a given context \(customer, currency, pricing rules, etc.\). The endpoint automatically applies eligibility rules to filter out ineligible catalogs and categories, ensuring that only offerings qualified for the requesting customer are returned.**Note:** This REST API wraps the [CatalogSearchAPI – getEligibleCatalogCategoryHierarchy\(Object input\)](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-getCatHierarchy&family=australia&ft:locale=en-US) JavaScript API.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

 

</td><td>

2026-08

</td><td>

[Reassign Assessment API](https://www.servicenow.com/docs/access?context=reassign-assessment-api&family=australia&ft:locale=en-US)

</td><td>

The new Reassign Assessment API provides a streamlined way to transfer assessment ownership within Smart Assessment workflows. This endpoint enables dynamic reassignment of in-progress assessments when team members change roles, leave the organization, or when assessments need to be delegated to more appropriate team members.

</td></tr><tr><td>

AI Control Tower

</td><td>

v6.0.0

</td><td>

2026-07

</td><td>

[AI Assets Inventory API](https://www.servicenow.com/docs/access?context=ai-assets-inventory-api&family=australia&ft:locale=en-US)

</td><td>

-   GET /asset-class
-   GET /details

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

v1.0

</td><td>

2026-07

</td><td>

[HL7 Inbound API](https://www.servicenow.com/docs/access?context=hl7-inbound-api&family=australia&ft:locale=en-US)

</td><td>

POST /message

</td></tr><tr><td>

Product Catalog Management

</td><td>

v20.0

</td><td>

2026-07

</td><td>

[Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US)

</td><td>

POST /api/sn\_prd\_pm/catalog/search**Note:** This REST API wraps the [CatalogSearchAPI – getEligibleCatalogCategoryHierarchy\(Object input\)](https://www.servicenow.com/docs/access?context=CatalogSearchAPI-getCatHierarchy&family=australia&ft:locale=en-US) JavaScript API.

</td></tr><tr><td>

Usage Insight Data Export

</td><td>

1.0.1

</td><td>

2026-07

</td><td>

[UXA Data Export Service API](https://www.servicenow.com/docs/access?context=usage-insight-data-exp-api&family=australia&ft:locale=en-US)

</td><td>

POST /sn\_uxa\_data\_export/data\_export

</td></tr><tr><td>

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

</td></tr><tr><td>

[KafkaProducerAPI - Scoped](https://www.servicenow.com/docs/access?context=KafkaProducerAPIScoped&family=australia&ft:locale=en-US)

</td><td>

-   KafkaProducerAPI\(\)
-   send\(\)

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

</td></tr><tr><td>

[Custom Connector Gateway API](https://www.servicenow.com/docs/access?context=custom-connector-gateway-api&family=australia&ft:locale=en-US)

</td><td>

-   POST /xcc-ingest \(ADDDOCUMENT\)
-   POST /xcc-ingest \(ADDPRINCIPAL\)
-   POST /xcc-ingest \(DELETEALLDOCUMENTS\)
-   POST /xcc-ingest \(DELETEALLPRINCIPALS\)
-   POST /xcc-ingest \(DELETEBYQUERY\)
-   POST /xcc-ingest \(DELETEDOCUMENT\)
-   POST /xcc-ingest \(DELETEPRINCIPAL\)

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://www.servicenow.com/docs/access?context=warranty-claims-SOAP-API&family=australia&ft:locale=en-US)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

</td></tr><tr><td>

Brazil

</td><td>

-   ****

    |Application|App Version|API type|API|Methods/Endpoints|
    |-----------|-----------|--------|---|-----------------|
    |Mobile SDK Libraries - Android|2.26.0|Mobile SDK|[NowChatConfiguration class - Android](https://www.servicenow.com/docs/access?context=NowChatOptionsAndroid&family=brazil&ft:locale=en-US)|VoiceInputButton\(\)|
    |Mobile SDK Libraries - iOS|2.26.0|Mobile SDK|[NowChatConfiguration class - iOS](https://www.servicenow.com/docs/access?context=NowChatOptionsiOS&family=brazil&ft:locale=en-US)|VoiceInputButton\(\)|
    |Zero Copy Connector for ERP \(com.snc.sn\_erp\_integration\)|10.6.0|Server|[sn\_erp\_integration API - Scoped, Global](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&family=brazil&ft:locale=en-US)|getRowCount\(\)|


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

Australia

</td><td>

<table><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

Module

</th><th>

Types

</th></tr></thead><tbody><tr><td>

Mobile SDK Libraries - Android

</td><td>

2.24.0

</td><td>

2026-08

</td><td>

-   NowChat
-   NowWeb

</td><td>

Default colors for [NowChatTheme interface - Android](https://www.servicenow.com/docs/access?context=NowChatThemeColorsAndroidInterface&family=australia&ft:locale=en-US) and [NowWebTheme interface - Android](https://www.servicenow.com/docs/access?context=NowWebThemeAndroidInterface&family=australia&ft:locale=en-US) now use the Coral theme.

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.24.0

</td><td>

2026-08

</td><td>

NowUIColoring

</td><td>

Default colors for [NowUIColoring](https://www.servicenow.com/docs/access?context=mobsdk-ios-use_nowUIcoloring&family=australia&ft:locale=en-US) now use the Coral theme.

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.22.0

</td><td>

2026-06

</td><td>

NowChat

</td><td>

New properties on [NowChatConfiguration class - iOS](https://www.servicenow.com/docs/access?context=NowChatOptionsiOS&family=australia&ft:locale=en-US) enable NowChat to integrate with NowVoice:-   **voiceConfiguration**
-   **voiceUIConfiguration**
-   **voiceCallbacks**

</td></tr></tbody>
</table>The following tables lists changed API classes and methods in Australia and ServiceNow Store.

 <table><thead><tr><th>

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

Lead to Cash Core

</td><td>

v1.8

</td><td>

2026-03

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=australia&ft:locale=en-US)

</td><td>

The following enhancements provide support for building and committing complete, ramp entity structures across header and headerless workflows:-   [LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)](https://www.servicenow.com/docs/access?context=LTCC-createInstance_S_S_B_O_B&family=australia&ft:locale=en-US): This method now supports selective record retrieval and multiple root entity definitions, enabling developers to explicitly fetch and aggregate ramp data in both single‑ and multi‑select, headerless scenarios.
-   [LeadtoCashCore - commitInstance\(Object targetJSON, Object additionalParams\)](https://www.servicenow.com/docs/access?context=LTCC-commitInstance_O_O&family=australia&ft:locale=en-US): This method now returns a structured `dataObject` that preserves all committed root entities grouped by type, enabling reliable access to ramp data from a single commit response without custom post‑processing.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v1.9

</td><td>

2026-06

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=australia&ft:locale=en-US)

</td><td>

[LeadtoCashCore - commitInstance\(Object targetJSON, Object additionalParams\)](https://www.servicenow.com/docs/access?context=LTCC-commitInstance_O_O&family=australia&ft:locale=en-US)- Added an optional `additionalParams.returnDeletedGr` Boolean flag that, when set to `true`, causes the deleted GlideRecord to be passed to `_postProcess` and `_postHierarchyCommit` after a DELETE operation.

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://www.servicenow.com/docs/access?context=c_GlideFormAPI&family=australia&ft:locale=en-US)

</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Read-only options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideFormAPINX&family=australia&ft:locale=en-US)

</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Read-only options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td></tr><tr><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=australia&ft:locale=en-US)

</td><td>

setICContext\(\) - New **searchTargetList.quickStats** object provides agent status information.

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

Customer Service Management \(CSM\)

</td><td>

v1.2

</td><td>

2026-07

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=australia&ft:locale=en-US)

</td><td>

setICContext\(\):

-   added `activeConversations` and `agentSettings` are added as new context inputs.

 subscribe\(\): Added openframe\_awa\_workitem\_cancelled as a new event.

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&family=australia&ft:locale=en-US)

</td><td>

POST /now/attachment/file now returns `403 Forbidden` instead of `401 Unauthorized` when access is denied at the ACL layer. To authenticate with this API, use OAuth 2.0 or enable preemptive authentication on the REST client. For more information, see [KB3054410](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3054410).

</td></tr><tr><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&family=australia&ft:locale=en-US)

</td><td>

Previously, all GET endpoints didn't return results for Account records as expected due to a hardcoded flag. As a fix, users are now required to install the plugin Customer Service Base Entities \(com.snc.cs\_base\), which adds the Active field to Customer \[customer\_account\] and Core Company \[core\_company\] tables.-   [Party Management – GET /api/sn\_tmf\_api/v1/party/individual](https://www.servicenow.com/docs/access?context=partymgmt-GET-individual&family=australia&ft:locale=en-US)
-   [Party Management - GET /api/sn\_tmf\_api/v1/party/individual/\{id\}](https://www.servicenow.com/docs/access?context=partymgmt-GET-individual-id&family=australia&ft:locale=en-US)
-   [Party Management – GET /api/ sn\_tmf\_api/v1/party/organization/\{id\}](https://www.servicenow.com/docs/access?context=partymgmt-GET-organization-id&family=australia&ft:locale=en-US)
-   [Party Management - GET /api/sn\_tmf\_api/v1/party/organization](https://www.servicenow.com/docs/access?context=partymgmt-GET-organization&family=australia&ft:locale=en-US)

</td></tr><tr><td>

[Wrap Up API](https://www.servicenow.com/docs/access?context=wrap-up-api&family=australia&ft:locale=en-US)

</td><td>

Added support for AI-generated wrap‑up codes and notes.-   [Wrap Up - GET /now/wrapup/segment/\{segment\_id\}](https://www.servicenow.com/docs/access?context=wrap-up-GET-segment&family=australia&ft:locale=en-US)
-   [Wrap Up - GET /now/wrapup/segment/agent/\{agent\_id\}/interaction/\{interaction\_id\}](https://www.servicenow.com/docs/access?context=wrap-up-GET-segment-agent-int&family=australia&ft:locale=en-US)
-   [Wrap Up - POST /now/wrapup/segment/create](https://www.servicenow.com/docs/access?context=wrap-up-POST-segment-create&family=australia&ft:locale=en-US)
-   [Wrap Up - PUT /now/wrapup/segment/update/ai](https://www.servicenow.com/docs/access?context=wrap-up-PUT-segment-update-ai&family=australia&ft:locale=en-US)

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

Telecommunications Open APIs \(sn\_tmf\_api\)

</td><td>

v7.2.0

</td><td>

2026-08

</td><td>

Updated APIs:

-   [Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&family=australia&ft:locale=en-US)
-   [Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=australia&ft:locale=en-US)
-   [Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=australia&ft:locale=en-US)
-   [Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=australia&ft:locale=en-US)
-   [Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&family=australia&ft:locale=en-US)
-   [Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=australia&ft:locale=en-US)

</td><td>

These TMF APIs are updated with the following:

1.  You can now safely customize TMF API behavior for your business needs, without modifying ServiceNow®'s default code or risking conflicts when you upgrade. Custom extensions automatically inherit all version-specific logic \(such as external ID fields in responses\), ensuring your integrations always work correctly. This V2 pattern works the same way across all TMF APIs, so you get a predictable, documented approach whether you're customizing one API or several. Existing V1 APIs and integrations are unaffected.

**Note:** By default, the product ships with V1 as the default version. Any API calls to the standard URL use V1 logic. If you want to use V2, you have two options:

    -   Toggle the "Is default" checkbox in the sys\_ws\_definition record to make V2 the default for all calls.
    -   Call the version-specific V2 URL directly from your integration source.
2.  **externalId** is now returned in V2 GET/LIST responses.

</td></tr><tr><td>

Telecommunications Open APIs \(sn\_tmf\_api\)

</td><td>

v7.2.0

</td><td>

2026-08

</td><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&family=australia&ft:locale=en-US)

</td><td>

This release contains two updates to the Party Management Open API:

 1.  The Party Management Open API has been updated to align with TMF 632 CTK \(Core Transaction Kernel\) compliance standards. The `PartyOrPartyRole` object has been removed and replaced with a mandatory `@type` field at the root level to explicitly declare party type \(`Account`, `Consumer`, or `Contact`\). The `relatedParty` object now includes a mandatory `@type` field to align with the latest TMF 632 schema. For migration guidance, see the related documentation.
2.  Supports inline creation and association of Contact and Location records during organization creation in a single request, eliminating the need for separate POST operations. The `mediumType` field has been renamed to `contactType` \(with `fax` renamed to `faxPhone`\); update any existing integrations accordingly. Organization responses now include `createdDate` and `lastModifiedDate` audit timestamps, plus support for `organizationChildRelationship` and `organizationParentRelationship` fields for organizational hierarchies.

</td></tr><tr><td>

Virtual Agent \(sn\_va\_as\_service\)

</td><td>

v4.4.0

</td><td>

2026-08

</td><td>

[Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&family=australia&ft:locale=en-US)

</td><td>

Now supports synchronous responses for the START\_CREATED\_CONVERSATION and CREATE\_CONVERSATION actions. By setting the **syncResponse** parameter to `true` in the request body,

-   CREATE\_CONVERSATION: Callers receive the conversation ID and interaction details in the API response, ensuring the conversation is fully initialized before the response is returned.
-   START\_CREATED\_CONVERSATION: Prevents potential race conditions and timing issues, for example when using the AWA Offer Work API.

</td></tr><tr><td>

Automated Test Framework

</td><td>

v3.1

</td><td>

2026-07

</td><td>

[Cloud Runner Test Runner REST API](https://www.servicenow.com/docs/access?context=cloudrunner-testrunner-api&family=australia&ft:locale=en-US)

</td><td>

The following endpoints are updated as follows:

-   POST /test\_runner: Now supports asynchronous test execution via the new `sync` parameter.
-   POST /cancel\_test\_runner: Introduces `rootTrackerId` as an alternative identifier for tracking and canceling test runs.
-   GET /test\_runner\_progress: Introduces `rootTrackerId` as an alternative identifier for tracking and canceling test runs.

 All Cloud Runner Test REST APIs now standardize on HTTP error codes: 400 for validation errors and 500 for unexpected errors.

</td></tr><tr><td>

Synthetic monitoring

</td><td>

1.7.1

</td><td>

2026-07

</td><td>

[SyntheticsAsyncBulkCreate API](https://www.servicenow.com/docs/access?context=synth-async-api&family=australia&ft:locale=en-US)

</td><td>

Updated functionality for POST /synthetics\_async\_bulk\_create: -   Checks for uniqueness against existing monitors on the fields **name**, **url**, **location**, **valid\_http\_code**, and **valid\_http\_code\_type** to avoid creating duplicates.
-   Request parameters **parent\_service\_sys\_id** and **support\_group\_sys\_id** are no longer required for endpoints that have a parent service relationship in the CI Relationship \[cmdb\_rel\_ci\] table.

</td></tr><tr><td>

Telecommunications Service Management

</td><td>

v4.1.1

</td><td>

2026-07

</td><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&family=australia&ft:locale=en-US)

</td><td>

The POST /organization endpoint now supports a list of valid **partyCharacteristic.name** values.As a result, the **partyCharacteristic.value** attribute accepts the display value of `rankTier` and `industry` choice fields as input. Invalid choice values trigger a descriptive warning in the API response, enabling clearer validation feedback and improved data consistency.

</td></tr><tr><td>

Order Management for Telecommunications

</td><td>

v4.0

</td><td>

2026-07

</td><td>

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=australia&ft:locale=en-US)

</td><td>

For all endpoints, the **serviceOrderItem.orderRelationship** parameter is renamed to **serviceOrderItem.serviceOrderItemRelationship**. This change affects both requests and responses.

</td></tr><tr><td>

Order Management for Telecommunications

</td><td>

v12.5.0

</td><td>

2026-06

</td><td>

-   [Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=australia&ft:locale=en-US)
-   [Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=australia&ft:locale=en-US)

</td><td>

The **characteristicObj** parameter is introduced as a fix to validate the **.value** property against allowed choice-type values by default. If an invalid value is submitted, the API adds a work note to the record.A new system property, `sn_ind_tmt_orm.disableCharValueValidation`, allows you to revert to pre-fix behavior when needed. The property isn't shipped by default. To turn off validation, create a system property named `sn_ind_tmt_orm.disableCharValueValidation` and set the value to `true`. When turned off, the value is set directly from the request payload and no work notes are generated.

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

v1.0

</td><td>

2026-05

</td><td>

[WSD Reservation API](https://www.servicenow.com/docs/access?context=wsd_reservation-api&family=australia&ft:locale=en-US)

</td><td>

In the POST /add endpoint, the **reservable\_module** request parameter is no longer required as of this release, but is required for earlier releases.

</td></tr></tbody>
</table>

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

Methods/Endpoints

</th></tr></thead><tbody><tr><td>

Customer Service Management

</td><td>

6.7.5

</td><td>

REST

</td><td>

[Trouble Ticket Open API](https://www.servicenow.com/docs/access?context=trouble-ticket-open-api&family=brazil&ft:locale=en-US)

</td><td>

**Important:** Migration Notice

Starting with the November 2026 release, the Trouble Ticket API transitions scope to Telecom Service Management Core \(`sn_ind_tsm_core`\) from SD-WAN \(`sn_ind_tsm_sdwan`\). Existing `sn_ind_tsm_sdwan` endpoints remain available but are deprecated until the Denmark release.Migrate your integrations to the new endpoints before the Denmark release to avoid disruption. See Trouble Ticket Open API documentation for timeline and migration guidance.

</td></tr><tr><td>

Customer Service Management

</td><td>

6.7.5

</td><td>

Server

</td><td>

[TroubleTicketNotificationUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=TroubleTicketNotifScopedAPI&family=brazil&ft:locale=en-US)

</td><td>

Starting with the November 2026 release, Trouble Ticket APIs transitions scope from `sn_ind_tsm_sdwan` to `sn_ind_tsm_core`. An automatic upgrade is planned for the December release for existing customers whose instances use S-DWAN.

</td></tr><tr><td>

Customer Service Management

</td><td>

1.8.0

</td><td>

REST

</td><td>

[\[Placeholder link text to key openframe-POST-voice-interaction\]](https://www.servicenow.com/docs/access?context=openframe-POST-voice-interaction&family=brazil&ft:locale=en-US)

</td><td>

POST /openframe/voice-interaction endpoint now returns an existing callback interaction instead of creating a new one when the first item in the **relatedRecords** array is an interaction record. This helps avoid duplicate interaction records when an agent calls a customer back from a callback interaction. The response includes the sys\_id and number of the existing interaction.

</td></tr></tbody>
</table>
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

Methods/Endpoints

</th></tr></thead><tbody><tr><td>

Universal MCP Client

</td><td>

1.1.3

</td><td>

Server

</td><td>

[MCPClient - Scoped](https://www.servicenow.com/docs/access?context=MCPClientAPI&family=brazil&ft:locale=en-US)

</td><td>

A new parameter **caller\_product** is added to specify the scope name of the application making the API call. This parameter is required for the following methods.-   getServers\(\)
-   getToolInfo\(\)
-   invokeTool\(\)
-   listTools\(\)


</td></tr><tr><td>

Mobile SDK Libraries - Android

</td><td>

2.26.0

</td><td>

Mobile SDK

</td><td>

[NowChatConfiguration class - Android](https://www.servicenow.com/docs/access?context=NowChatOptionsAndroid&family=brazil&ft:locale=en-US)

</td><td>

New optional parameters added to UIConfiguration\(\).-   **hideServiceNowInProductBranding**: Show or hide ServiceNow branding in Virtual Agent.
-   **voiceInputButton**: Show or hide the speech-to-text microphone button in the text input bar.


</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.26.0

</td><td>

Mobile SDK

</td><td>

[NowChatConfiguration class - iOS](https://www.servicenow.com/docs/access?context=NowChatOptionsiOS&family=brazil&ft:locale=en-US)

</td><td>

New optional parameters added to UIConfiguration\(\).-   **hideBranding**: Show or hide ServiceNow branding in Virtual Agent.
-   **voiceInputButton**: Show or hide the speech-to-text microphone button in the text input bar.


</td></tr><tr><td>

Order Management for Telecommunications and Media

</td><td>

15.0.4

</td><td>

REST

</td><td>

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=brazil&ft:locale=en-US)

</td><td>

The PATCH `/sn_ind_tmt_orm/order/productOrder/{id}` endpoint now accepts the V3 `relatedParty` item shape \(`role`/`@type`/`partyOrPartyRole`\). PATCH supports only the reference pattern for both V2 and V3 versions of the API.

</td></tr><tr><td>

Telecommunications Service Management

</td><td>

8.0.3

</td><td>

REST

</td><td>

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=brazil&ft:locale=en-US)

</td><td>

In the GET /product and GET /\{id\} endpoints, the `productCharacteristic.valueType` field now supports a new `sn_prd_invt.enableseamlessvaluetype` system property that, when enabled, returns the same backend value format the Product Order API already uses, allowing consistent characteristic value types across both APIs.

</td></tr><tr><td>

Omnichannel Callback for Customer Service Management \(sn\_callback\)

</td><td>

1.8.3

</td><td>

REST

</td><td>

[Voice Interaction Resource API](https://www.servicenow.com/docs/access?context=voice-interaction-resource-api&family=brazil&ft:locale=en-US)

</td><td>

The `POST /api/now/openframe/voice-interaction` endpoint now prevents duplicate interactions by reusing existing work-in-progress callbacks when an agent clicks to call from the workspace. The system checks for WIP interactions with matching `inbound_id` and parties before creating a new record, and accepts a new `relatedRecords` objecy to pass callback context via `context_document` and `context_table` fields.

</td></tr></tbody>
</table>
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

Methods/Endpoints

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

Australia

</td><td>

-   NowAnalyticsService, NowAnalyticsServiceDelegate, and SNMobileAnalytics have been removed from Mobile SDK - iOS.
-   NowAnalyticsSDK has been removed from Mobile SDK - Android.

 -   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

</td></tr><tr><td>

Brazil

</td><td>

-   **Trouble Ticket Open API**

[Trouble Ticket Open API](https://www.servicenow.com/docs/access?context=trouble-ticket-open-api&family=brazil&ft:locale=en-US) endpoints under the `sn_ind_tsm_sdwan` scope are deprecated but remain available until the Denmark release, at which point they will be officially removed and inaccessible. Endpoints use a new `sn_ind_tsm_core` scope as of the November 2026 release. See Trouble Ticket documentation for migration guidance and timeline information.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **Activation information**

API activation is dependent on the specific product or application where the API is required. Consult your product documentation or contact your ServiceNow® administrator to determine activation steps for your use case.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

 See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

