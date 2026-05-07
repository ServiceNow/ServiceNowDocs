---
title: API release notes
description: ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# API release notes

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Australia release.

## API highlights for the Australia release

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&version=australia&pubname=australia-api-reference&ft:locale=en-US) for more information.

## New in the Australia release

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[GlideAggregate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideAggregateScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>

[GlideDate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideDateScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideTime - Scoped](https://www.servicenow.com/docs/access?context=c_GlideTimeScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   getDisplayValueLang\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)

</td></tr><tr><td>

[GlideElementDescriptor - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

[GlideElementDescriptor - isEncrypted\(\)](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&version=australia&pubname=australia-api-reference&section=SGED-isEncrypted&ft:locale=en-US)

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

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>

[ConsolidationService - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsolidationServiceAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

setAggregateWorkflow\(\)

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideElement - Global](https://www.servicenow.com/docs/access?context=c_GlideElementAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

getDynamicNamespace\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributePathsInSchema\(\)
-   getDynamicAttributePathsInStore\(\)
-   getDynamicNamespaceName\(\)

</td></tr><tr><td>

[MIDHermesProducer - Global](https://www.servicenow.com/docs/access?context=MIDHermesProducerAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   MIDHermesProducer\(\)
-   send\(\)

</td></tr><tr><td>

[GlideElementDescriptor - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

[GlideElementDescriptor - isEncrypted\(\)](https://www.servicenow.com/docs/access?context=c_GlideElementDescriptorScopedAPI&version=australia&pubname=australia-api-reference&section=SGED-isEncrypted&ft:locale=en-US)

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

Lead to Cash Core

</td><td>

v0.1

</td><td>

2026-05

</td><td>

[ConsolidationService - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsolidationServiceAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes
-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachments/\{attachment\_sys\_id\}/attributes
-   PATCH /now/attachment/\{sys\_id\}
-   POST /now/attachment/\{attachment\_sys\_id\}/attributes
-   PUT /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}

</td></tr><tr><td>

[Help Request API](https://www.servicenow.com/docs/access?context=help-request-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

POST /now/helprequest/action/create\_or\_update

</td></tr><tr><td>

[ATF Code Coverage API](https://www.servicenow.com/docs/access?context=atf-code-coverage-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   POST /now/atf/code\_coverage/all
-   POST /now/atf/code\_coverage/by\_line\_number
-   POST /now/atf/code\_coverage/by\_script\_id

</td></tr><tr><td>

[Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>

[WSD Presence API](https://www.servicenow.com/docs/access?context=wsd_presence-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[WSD User API](https://www.servicenow.com/docs/access?context=wsd_user-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

GET /context

</td></tr><tr><td>

Workplace Service Delivery

</td><td>

3.3.1

</td><td>

2026-05

</td><td>

[WSD Unified Search API](https://www.servicenow.com/docs/access?context=wsd_unified-search-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

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

[SyntheticsAsyncBulkCreate API](https://www.servicenow.com/docs/access?context=synth-async-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   GET /synthetics\_async\_bulk\_create/\{job\_id\}
-   POST /synthetics\_async\_bulk\_create

</td></tr><tr><td>

Synthetic monitoring

</td><td>

1.5.1

</td><td>

2026-03

</td><td>

[SyntheticsBulkCreate API](https://www.servicenow.com/docs/access?context=synthetics-bulk-create-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

POST /synthetics\_bulk\_create

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://www.servicenow.com/docs/access?context=warranty-claims-SOAP-API&version=australia&pubname=australia-manufacturing&ft:locale=en-US)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

## Changed in this release

The following tables lists changed API classes and methods in Australia and ServiceNow Store.

<table id="table_gbh_3zx_x3c"><thead><tr><th>

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

v1.8

</td><td>

2026-03

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

The following enhancements provide support for building and committing complete, ramp entity structures across header and headerless workflows:-   [LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=australia&pubname=australia-api-reference&section=LTCC-createInstance_S_S_B_O_B&ft:locale=en-US): This method now supports selective record retrieval and multiple root entity definitions, enabling developers to explicitly fetch and aggregate ramp data \(for example, via **fetchRecordSysIds** and **multiSelectMerge**\) in both single‑ and multi‑select, headerless scenarios.
-   [LeadtoCashCore - commitInstance\(Object targetJSON, Object additionalParams\)](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=australia&pubname=australia-api-reference&section=LTCC-commitInstance_O_O&ft:locale=en-US): This method now returns a structured `dataObject` that preserves all committed root entities—such as Sold Products and Ramps—grouped by type, enabling reliable access to ramp data from a single commit response without custom post‑processing.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://www.servicenow.com/docs/access?context=c_GlideFormAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideFormAPINX&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

On fields set to strict read only, the following methods do nothing and log a warning in the browser's console if used:-   clearValue\(\)
-   setValue\(\)

For more information, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|API|Endpoints|
|---|---------|
|[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)|setICContext\(\) - New **searchTargetList.quickStats** object provides agent status information.|

<table id="table_lcz_gmc_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Previously, all GET endpoints didn't return results for Account records as expected due to a hardcoded flag. As a fix, users are now required to install the plugin Customer Service Base Entities \(com.snc.cs\_base\), which adds the Active field to Customer \[customer\_account\] and Core Company \[core\_company\] tables.-   [Party Management – GET /api/sn\_tmf\_api/v1/party/individual](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=australia&pubname=australia-api-reference&section=partymgmt-GET-individual&ft:locale=en-US)
-   [Party Management - GET /api/sn\_tmf\_api/v1/party/individual/\{id\}](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=australia&pubname=australia-api-reference&section=partymgmt-GET-individual-id&ft:locale=en-US)
-   [Party Management – GET/api/ sn\_tmf\_api/v1/party/organization/\{id\}](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=australia&pubname=australia-api-reference&section=partymgmt-GET-organization-id&ft:locale=en-US)
-   [Party Management - GET /api/sn\_tmf\_api/v1/party/organization](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=australia&pubname=australia-api-reference&section=partymgmt-GET-organization&ft:locale=en-US)

</td></tr><tr><td>

[Wrap Up API](https://www.servicenow.com/docs/access?context=wrap-up-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Added support for AI-generated wrap‑up codes and notes.-   [Wrap Up - GET /now/wrapup/segment/\{segment\_id\}](https://www.servicenow.com/docs/access?context=wrap-up-api&version=australia&pubname=australia-api-reference&section=wrap-up-GET-segment&ft:locale=en-US)
-   [Wrap Up - GET /now/wrapup/segment/agent/\{agent\_id\}/interaction/\{interaction\_id\}](https://www.servicenow.com/docs/access?context=wrap-up-api&version=australia&pubname=australia-api-reference&section=wrap-up-GET-segment-agent-int&ft:locale=en-US)
-   [Wrap Up - POST /now/wrapup/segment/create](https://www.servicenow.com/docs/access?context=wrap-up-api&version=australia&pubname=australia-api-reference&section=wrap-up-POST-segment-create&ft:locale=en-US)
-   [Wrap Up - PUT /now/wrapup/segment/update/ai](https://www.servicenow.com/docs/access?context=wrap-up-api&version=australia&pubname=australia-api-reference&section=wrap-up-PUT-segment-update-ai&ft:locale=en-US)

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

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

