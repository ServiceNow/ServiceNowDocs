---
title: API release notes
description: ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# API release notes

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

## API highlights for the Australia release

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See  for more information.

## New in the Australia release

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>



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



</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>



</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>



</td><td>

-   getDisplayValueEx\(\)
-   getDisplayValueLang\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)

</td></tr><tr><td>



</td><td>



</td></tr></tbody>
</table><table id="table_nds_wxf_gfc"><thead><tr><th>

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

v20.0

</td><td>

2026-07

</td><td>



</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named, the `CatalogSearch` Server API is the base platform API for service catalog item search; the new `CatalogSearchAPI` is a higher-level wrapper specifically for the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The REST version of this API is .

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>



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
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>



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



</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>



</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>



</td><td>

getDynamicNamespace\(\)

</td></tr><tr><td>



</td><td>

-   getDynamicAttributePathsInSchema\(\)
-   getDynamicAttributePathsInStore\(\)
-   getDynamicNamespaceName\(\)

</td></tr><tr><td>



</td><td>

-   MIDHermesProducer\(\)
-   send\(\)

</td></tr><tr><td>



</td><td>



</td></tr></tbody>
</table><table id="table_bps_p1y_x3c"><thead><tr><th>

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

v20.0

</td><td>

2026-07

</td><td>



</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named, the `CatalogSearch` Server API is the base platform API for service catalog item search; the new `CatalogSearchAPI` is a higher-level wrapper specifically for the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The REST version of this API is .

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>



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
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>



</td><td>

-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes
-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachments/\{attachment\_sys\_id\}/attributes
-   PATCH /now/attachment/\{sys\_id\}
-   POST /now/attachment/\{attachment\_sys\_id\}/attributes
-   PUT /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}

</td></tr><tr><td>



</td><td>

POST /now/helprequest/action/create\_or\_update

</td></tr><tr><td>



</td><td>

-   POST /now/atf/code\_coverage/all
-   POST /now/atf/code\_coverage/by\_line\_number
-   POST /now/atf/code\_coverage/by\_script\_id

</td></tr><tr><td>



</td><td>

-   POST /api/sn\_csm\_pricing/\{api\_version\}/pricingengine/computePrice
-   DELETE /api/sn\_csm\_pricing/pricingengine/pricing\_context/\{pricing\_context\_id\}

</td></tr></tbody>
</table><table id="table_a22_gjw_bjc"><thead><tr><th>

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

AI Control Tower

</td><td>

v6.0.0

</td><td>

2026-07

</td><td>



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



</td><td>

POST /message

</td></tr><tr><td>

Product Catalog Management

</td><td>

v20.0

</td><td>

2026-07

</td><td>



</td><td>

POST /api/sn\_prd\_pm/catalog/search**Note:** The script include version of this API is .

</td></tr><tr><td>

Usage Insight Data Export

</td><td>

1.0.1

</td><td>

2026-07

</td><td>



</td><td>

POST /sn\_uxa\_data\_export/data\_export

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>



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



</td><td>

GET /context

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>



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



</td><td>

-   GET /synthetics\_async\_bulk\_create/\{job\_id\}
-   POST /synthetics\_async\_bulk\_create

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/warranty-claims-SOAP-API.md)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

## Changed in this release

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

|Application|App Version|Release month|API|Methods|
|-----------|-----------|-------------|---|-------|

<table id="table_gbh_3zx_x3c"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

API

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

v1.8

</td><td>

2026-03

</td><td>



</td><td>

The following enhancements provide support for building and committing complete, ramp entity structures across header and headerless workflows:-   : This method now supports selective record retrieval and multiple root entity definitions, enabling developers to explicitly fetch and aggregate ramp data \(for example, via **fetchRecordSysIds** and **multiSelectMerge**\) in both single‑ and multi‑select, headerless scenarios.
-   : This method now returns a structured `dataObject` that preserves all committed root entities—such as Sold Products and Ramps—grouped by type, enabling reliable access to ramp data from a single commit response without custom post‑processing.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

v1.9

</td><td>

2026-06

</td><td>



</td><td>

- Added an optional `additionalParams.returnDeletedGr` Boolean flag that, when set to `true`, causes the deleted GlideRecord to be passed to `_postProcess` and `_postHierarchyCommit` after a DELETE operation.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>



</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/read-only-option.md).

</td></tr><tr><td>



</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/read-only-option.md).

</td></tr><tr><td>



</td><td>

setICContext\(\) - New **searchTargetList.quickStats** object provides agent status information.

</td></tr></tbody>
</table><table id="table_changed_client_APIs"><thead><tr><th>

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

Customer Service Management \(CSM\)

</td><td>

v1.2

</td><td>

2026-07

</td><td>



</td><td>

setICContext\(\):

-   added `activeConversations` and `agentSettings` are added as new context inputs.

 subscribe\(\): Added openframe\_awa\_workitem\_cancelled as a new event.

</td></tr></tbody>
</table><table id="table_lcz_gmc_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>



</td><td>

Previously, all GET endpoints didn't return results for Account records as expected due to a hardcoded flag. As a fix, users are now required to install the plugin Customer Service Base Entities \(com.snc.cs\_base\), which adds the Active field to Customer \[customer\_account\] and Core Company \[core\_company\] tables.-   
-   
-   
-   

</td></tr><tr><td>



</td><td>

Added support for AI-generated wrap‑up codes and notes.-   
-   
-   
-   

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

Automated Test Framework

</td><td>

v3.1

</td><td>

2026-07

</td><td>



</td><td>

The following endpoints are updated as follows:

-   POST /test\_runner: Now supports asynchronous test execution via the new `sync` parameter.
-   POST /cancel\_test\_runner: Introduces `rootTrackerId` as an alternative identifier for tracking and canceling test runs.
-   GET /test\_runner\_progress: Introduces `rootTrackerId` as an alternative identifier for tracking and canceling test runs.

 All Cloud Runner Test REST APIs now standardize on HTTP error codes: 400 for validation errors and 500 for unexpected errors.

</td></tr><tr><td>

Telecommunications Service Management

</td><td>

v4.1.1

</td><td>

2026-07

</td><td>



</td><td>

The POST /organization endpoint now supports a list of valid **partyCharacteristic.name** values.As a result, the **partyCharacteristic.value** attribute accepts the display value of `rankTier` and `industry` choice fields as input. Invalid choice values trigger a descriptive warning in the API response, enabling clearer validation feedback and improved data consistency.

</td></tr><tr><td>

Order Management for Telecommunications

</td><td>

v4.0

</td><td>

2026-07

</td><td>



</td><td>

For all endpoints, the **serviceOrderItem.orderRelationship** parameter is renamed to **serviceOrderItem.serviceOrderItemRelationship**. This change affects both requests and responses.

</td></tr><tr><td>

Order Management for Telecommunications

</td><td>

v12.5.0

</td><td>

2026-06

</td><td>

-   
-   

</td><td>

The **characteristicObj** parameter is introduced as a fix to validate the **.value** property against allowed choice-type values by default. If an invalid value is submitted, the API adds a work note to the record.A new system property, `sn_ind_tmt_orm.disableCharValueValidation`, allows you to revert to pre-fix behavior when needed. The property isn't shipped by default. To disable validation, create a system property named `sn_ind_tmt_orm.disableCharValueValidation` and set the value to `true`. When disabled, the value is set directly from the request payload and no work notes are generated.

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

v1.0

</td><td>

2026-05

</td><td>



</td><td>

In the POST /add endpoint, the **reservable\_module** request parameter is no longer required as of this release, but is required for earlier releases.

</td></tr></tbody>
</table>## Deprecations

-   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

## Activation information

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

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

