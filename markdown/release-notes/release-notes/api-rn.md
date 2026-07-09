---
title: API release notes
description: ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
---

# API release notes

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Zurich release.

## API highlights for the Zurich release

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See [API implementation and reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/api-implementation-reference.md) for more information.

## New in the Zurich release

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideCurrencyCode - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideCurrencyCodeBothAPI.md)

</td><td>

-   getCurrencyCode\(\)
-   getNumericCurrencyCode\(\)

</td></tr><tr><td>

[GlideCurrencySymbol - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideCurrencySymbolBothAPI.md)

</td><td>

-   getCurrencySymbol\(\)
-   getSortedActiveCurrencySymbols\(\)

</td></tr><tr><td>

[GlideQueryCondition - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideQueryConditionScopedAPI.md)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md)

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

[GlideSysAttachment - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideSysAttachmentScopedAPI.md)

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

[GlideSystem - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideSystemScopedAPI.md)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addSuccessMessage\(\)
-   addModerateMessage\(\)

</td></tr></tbody>
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideDynamicAttribute - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideDynamicAttributeAPI.md)

</td><td>

Updated content to remove support for dynamic attribute groups.New method getNamespaceName\(\).

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideDynamicAttStoreAPI.md)

</td><td>

Updated content to remove support for dynamic attribute groups.New methods:

-   getDynamicNamespace\(\)
-   setDynamicNamespace\(\)

</td></tr><tr><td>

[GlideDynamicNamespace - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideDynamicNamespaceAPI.md)

</td><td>

-   getName\(\)
-   isActive\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideQueryCondition - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideQueryConditionAPI.md)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideRecordAPI.md)

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

[GlideSysAttachment - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideSysAttachmentGlobalAPI.md)

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

[GlideSystem - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/c_GlideSystemAPI.md)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)

</td></tr><tr><td>

[Message - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/sn_i18n.messageAPI.md)

</td><td>

Retrieves localized messages from the Message \[sys\_ui\_message\] table. It supports internationalization \(i18n\) by dynamically fetching messages based on the user's session language or a specified language parameter.-   getMessage\(\)
-   getMessageLang\(\)

</td></tr></tbody>
</table><table id="table_nds_wxf_gfc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/c_GlideFormAPI.md)

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

[GlideModal \(Next Experience\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/GModClientAPINX.md)

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

[GlideNavigation \(Next Experience\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/GlideNavigationClientAPINX.md)

</td><td>

refreshNavigator\(\)

</td></tr><tr><td>

[StopWatch \(Next Experience\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/StopWatchAPINX.md)

</td><td>

-   StopWatch\(\)
-   getTime\(\)
-   restart\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/GlideFormAPINX.md)

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

[GlideUser \(Next Experience\) - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/GlideUserAPINX.md)

</td><td>

getRoles\(\)

</td></tr></tbody>
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Conversation Member API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/conversation-member-api.md)

</td><td>

-   PUT now/conversation/member/\{user\_id\}/drop
-   PUT now/conversation/member/\{user\_id\}/update

</td></tr><tr><td>

[Omnichannel Callback API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/omichannel-callback-api.md)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

[CSM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/csm-pricing-api.md)

</td><td>

-   POST /api/sn\_csm\_pricing/pricingengine/computePrice
-   DELETE /api/sn\_csm\_pricing/pricingengine/pricing\_context/\{pricing\_context\_id\}

</td></tr></tbody>
</table><table id="table_qlh_nlc_tcc"><thead><tr><th>

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

[Omnichannel Callback API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/omichannel-callback-api.md)

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

[External ID Mapping API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/external-id-mapping-api.md)

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

[Digital Product Release API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/digital-product-release-api.md)

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

[TISC TAXII Server API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/taxii-server-api.md)

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

[Party Management Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tmf-party-management-open-api.md)

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

[Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/product-inventory-open-api.md)

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

[Service Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/service-catalog-open-api.md)

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

[TISC Intel Exchange API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tisc-intel-ex-api.md)

</td><td>

POST /sn\_sec\_tisc/tisc\_intel\_sharing\_api/post\_intel

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC RPZ API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/tisc-rpz-api.md)

</td><td>

POST /sn\_sec\_tisc/rpz\_export

</td></tr><tr><td>

Network Inventory Advanced

</td><td>

10.0

</td><td>

2025-08

</td><td>

[DCIM Metric Data Feed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/dcim-metric-data-feed-api.md)

</td><td>

POST /api/sn\_ni\_adv/dcim/feed/\{vendorname\}

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.2

</td><td>

2025-08

</td><td>

[Omnichannel Callback API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/omichannel-callback-api.md)

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

[Quote Management API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/quote-management-api.md)

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

[Work Order Management API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/work-order-mgmt-api.md)

</td><td>

-   CANCEL /sn\_tmf\_api/work\_order\_management\_api/cancelWorkOrder
-   GET /sn\_tmf\_api/work\_order\_management\_api/workordermanagement
-   GET /sn\_tmf\_api/work\_order\_management\_api/workorder/\{id\}
-   PATCH /sn\_tmf\_api/work\_order\_management\_api/workOrder/\{id\}
-   POST /sn\_tmf\_api/work\_order\_management\_api/workOrder

</td></tr></tbody>
</table>## Changed in this release

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
</table>## Deprecations

-   The GlideEncrypter API no longer supports Triple Data Encryption Standard \(3DES\) due to updated [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) guidelines.
    -   For existing instances that upgrade to the Zurich release, the GlideEncrypter API is available for use but has been updated to automatically use the Key Management Framework algorithm. See [GlideEncrypter - Global \(deprecated\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideEncrypterAPI.md) for more information on how to continue calling this API.
    -   For all new instances created starting with the Zurich release, the GlideEncrypter API is no longer supported. Directly use the [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/encryption.md) instead for all cryptography operations.
-   Dynamic groups have been removed from dynamic schema in Core Platform. For dynamic attributes defined with an associated dynamic attribute group before the Zurich release, the [GlideDynamicAttribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/GlideDynamicAttributeAPI.md) getGroupName\(\) method originally designed for dynamic attribute groups continues to work for backwards compatibility.

    The getGroupName\(\) method returns null for migrated attributes and newly created attributes.

    Customers are urged to migrate to the current [Dynamic Attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/working-with-dynamic-schema.md) definitions to take advantage of future improvements in features and functionality. For migration details, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.


## Activation information

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

**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/new-features-changes.md)

