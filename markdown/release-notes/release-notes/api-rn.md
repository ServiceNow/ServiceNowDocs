---
title: API release notes
description: ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 10
---

# API release notes

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

## About API

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See  for more information.

## Activation and other requirements

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

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

## June 2026

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

### What's new

<table id="table_xcs_y5z_1kc"><thead><tr><th>

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

-   
-   
-   
-   
-   
-   
-   
-   

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.22.0

</td><td>

2026-06

</td><td>

NowVoice

</td><td>

-   
-   
-   
-   
-   
-   
-   
-   

</td></tr></tbody>
</table>### What's changed

<table id="table_jl3_1zz_1kc"><thead><tr><th>

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

Default colors for  and  now use the Coral theme.

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.24.0

</td><td>

2026-08

</td><td>

NowUIColoring

</td><td>

Default colors for NowUIColoring now use the Coral theme.

</td></tr><tr><td>

Mobile SDK Libraries - iOS

</td><td>

2.22.0

</td><td>

2026-06

</td><td>

NowChat

</td><td>

New properties on  enable NowChat to integrate with NowVoice:-   **voiceConfiguration**
-   **voiceUIConfiguration**
-   **voiceCallbacks**

</td></tr></tbody>
</table>## Australia General Availability

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

### What's new

<table id="table_a22_gjw_bjc"><thead><tr><th>

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



</td><td>

POST /eligible-catalog-category-hierarchy is a new endpoint that retrieves the complete product catalog-category hierarchy for a given context \(customer, currency, pricing rules, etc.\). The endpoint automatically applies eligibility rules to filter out ineligible catalogs and categories, ensuring that only offerings qualified for the requesting customer are returned.**Note:** This REST API wraps the  JavaScript API.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

 

</td><td>

2026-08

</td><td>



</td><td>

The new Reassign Assessment API provides a streamlined way to transfer assessment ownership within Smart Assessment workflows. This endpoint enables dynamic reassignment of in-progress assessments when team members change roles, leave the organization, or when assessments need to be delegated to more appropriate team members.

</td></tr><tr><td>

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

POST /api/sn\_prd\_pm/catalog/search**Note:** This REST API wraps the  JavaScript API.

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
</table>### What's deprecated or removed

-   NowAnalyticsService and NowAnalyticsServiceDelegate have been removed from Mobile SDK - iOS.
-   NowAnalyticsSDK has been removed from Mobile SDK - Android.

## Australia

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

### What's new

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



</td><td>

The new getEligibleCatalogCategoryHierarchy\(\) method lets you retrieve the complete product catalog-category hierarchy for a given context \(customer, currency, pricing rules, etc.\). The API automatically applies eligibility rules to filter out ineligible catalogs and categories, ensuring that customers see only the offerings they qualify for.**Note:** The REST version of this endpoint is .

</td></tr><tr><td>

Product Catalog Management

</td><td>

v20.0

</td><td>

2026-07

</td><td>



</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named to `CatalogSearch` Server API, the new `CatalogSearchAPI` is a higher-level wrapper specifically for the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The  REST API wraps this Server API.

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

</td></tr><tr><td>

MCP Client

</td><td>

v1.0.1

</td><td>

2026-05

</td><td>



</td><td>

-   MCPClient\(\)
-   getServers\(\)
-   getToolInfo\(\)
-   invokeTool\(\)
-   listTools\(\)

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



</td><td>

-   CatalogSearch\(\) constructor
-   getCatalogData\(\)

 Though identically named, to `CatalogSearch`, the new `CatalogSearchAPI` is used within the product catalog use case, with additional capabilities relevant to TMF-aligned product and service offerings.

 **Note:** The  REST API wraps this Server API.

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
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/warranty-claims-SOAP-API.md)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

### What's changed

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

<table id="table_gbh_3zx_x3c"><thead><tr><th>

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



</td><td>

The following enhancements provide support for building and committing complete, ramp entity structures across header and headerless workflows:-   : This method now supports selective record retrieval and multiple root entity definitions, enabling developers to explicitly fetch and aggregate ramp data in both single‑ and multi‑select, headerless scenarios.
-   : This method now returns a structured `dataObject` that preserves all committed root entities grouped by type, enabling reliable access to ramp data from a single commit response without custom post‑processing.

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

Telecommunications Open APIs \(sn\_tmf\_api\)

</td><td>

v7.2.0

</td><td>

2026-08

</td><td>

Updated APIs:

-   
-   
-   
-   
-   
-   

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

The **characteristicObj** parameter is introduced as a fix to validate the **.value** property against allowed choice-type values by default. If an invalid value is submitted, the API adds a work note to the record.A new system property, `sn_ind_tmt_orm.disableCharValueValidation`, allows you to revert to pre-fix behavior when needed. The property isn't shipped by default. To turn off validation, create a system property named `sn_ind_tmt_orm.disableCharValueValidation` and set the value to `true`. When turned off, the value is set directly from the request payload and no work notes are generated.

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
</table>### What's deprecated or removed

-   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.

