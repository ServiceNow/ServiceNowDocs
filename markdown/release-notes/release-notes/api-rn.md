---
title: API release notes
description: ServiceNow APIs let you build custom applications and experiences. APIs were enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
---

# API release notes

ServiceNow® APIs let you build custom applications and experiences. APIs were enhanced and updated in the Xanadu release.

## API highlights for the Xanadu release

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) for more information.

## New in the Xanadu release

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQBScopedScriptableAPI - Scoped](https://www.servicenow.com/docs/access?context=CMDBQBScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   getSavedQueryExecutionDetails\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDAutomationProvider - Scoped, Global](https://www.servicenow.com/docs/access?context=PDAutomationProviderBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   activateProcess\(\)
-   deactivateProcess\(\)
-   duplicateProcess\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr><tr><td>

[PersonalAuthAPI - Scoped](https://www.servicenow.com/docs/access?context=PersonalAuthAPIScoped&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   PersonalAuthAPI\(\)
-   getInitiatorURL\(\)
-   isTokenValid\(\)
-   revokeToken\(\)

</td></tr><tr><td>

[PlaybookExperience - Scoped](https://www.servicenow.com/docs/access?context=PlaybookExperienceScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

restartPlaybook\(\)

</td></tr></tbody>
</table><table id="table_lc5_sqn_xwb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQueryBuilderAPI - Global](https://www.servicenow.com/docs/access?context=CMDBQueryBuilderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[DynamicSchemaAPI - Global](https://www.servicenow.com/docs/access?context=DynamicSchemaAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   clearDynamicCategoryCache\(\)
-   clearDynamicChoiceSetCache\(\)
-   clearDynamicAttributeGroupCache\(\)
-   clearDynamicAttributeGroupCacheItem\(\)
-   clearDynamicCategoryCacheItem\(\)
-   clearDynamicChoiceSetItem\(\)
-   get\(\)

</td></tr><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

parseDate\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   clear\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   setDisplayValue\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setValue\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeDisplayValues\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\) - two signatures
-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValue\(\) - two signatures
-   setDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValues\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr></tbody>
</table><table id="table_g2w_k5d_mbc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[m\_form - Client](https://www.servicenow.com/docs/access?context=m_formClientAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   getValue\(\)
-   setAffectedInputs\(\)
-   setValue\(\)

</td></tr><tr><td>

[MobileScriptIncludeCaller - Client](https://www.servicenow.com/docs/access?context=MobileScriptInclCallerClientAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   MobileScriptIncludeCaller\(\)
-   addParam\(\)
-   call\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Cloud Services Catalog API](https://www.servicenow.com/docs/access?context=cs-catalog-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   GET /now/cmp\_catalog\_api/itemsbyciclass
-   GET /now/cmp\_catalog\_api/itemsbyrb
-   GET /now/cmp\_catalog\_api/services
-   GET /now/cmp\_catalog\_api/stacks
-   GET /now/cmp\_catalog\_api/status
-   POST /now/cmp\_catalog\_api/submitoprequest
-   POST /now/cmp\_catalog\_api/submitrequest

</td></tr><tr><td>

[Proactive Engagement API](https://www.servicenow.com/docs/access?context=proactive-engagement-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

CREATE /api/sn\_pren/self\_remediation/experience\_issue/create

</td></tr></tbody>
</table>|Application|App version|Class|Methods|
|-----------|-----------|-----|-------|
| | |[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|getAWAAgentPresence\(\)|

<table id="table_asg_kj5_zbc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td><td>

[sb - Scoped, Global](https://www.servicenow.com/docs/access?context=PSBPublicAPIUtilBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   archive\(\)
-   checkout\(\)
-   publish\(\)
-   retire\(\)

</td></tr></tbody>
</table><table id="table_lz3_nm5_zbc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td><td>

[sb - Scoped, Global](https://www.servicenow.com/docs/access?context=PSBPublicAPIUtilBoth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   archive\(\)
-   checkout\(\)
-   publish\(\)
-   retire\(\)

</td></tr></tbody>
</table><table id="table_nct_jxv_lbc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Accounts Payable Invoice Processing

</td><td>

V9.03

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   POST sn\_spend\_intg/ap\_invoice/cxml
-   POST sn\_spend\_intg/ap\_invoice/json

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V3.0.0

</td><td>

[Appointment Open API](https://www.servicenow.com/docs/access?context=appointment-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_tmf\_api/appointment/appointment
-   GET /sn\_tmf\_api/appointment/appointment/\{id\}
-   GET /sn\_tmf\_api/appointment/searchTimeSlot
-   DELETE /sn\_tmf\_api/appointment/appointment/\{id\}
-   PATCH /sn\_tmf\_api/appointment/appointment/\{id\}
-   POST /sn\_tmf\_api/appointment/appointment

</td></tr><tr><td>

Proactive Engagement

</td><td>

V1.0

</td><td>

[Proactive Engagement API](https://www.servicenow.com/docs/access?context=proactive-engagement-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

CREATE /sn\_pren/self\_remediation/experience\_issue/create

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   DELETE /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
-   DELETE /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
-   PATCH /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
-   PATCH /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Resource Inventory Open API](https://www.servicenow.com/docs/access?context=resource-inventory-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added support for Cable, Strand, and Topology tables. This change is reflected in the @type, id, and resourceRelationship.resource property descriptions.-   DELETE /sn\_ni\_core/resource/\{id\}
-   GET /sn\_ni\_core/resource
-   GET /sn\_ni\_core/resource/\{id\}
-   PATCH /sn\_ni\_core/resource/\{id\}
-   POST /sn\_ni\_core/resource
-   POST /sn\_ni\_core/resourceinventoryviatemplate

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Service Test Management Open API](https://www.servicenow.com/docs/access?context=service-test-management-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTest
-   GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTest/\{id\}
-   GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification
-   GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification/\{id\}
-   PATCH /sn\_sprb\_mgmt/servicetestmanagement/serviceTest/\{id\}
-   PATCH /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification/\{id\}
-   POST /sn\_sprb\_mgmt/servicetestmanagement/serviceTest
-   POST /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

V3.5.0

</td><td>

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/threat\_intel\_data/add\_observables

</td></tr></tbody>
</table>## Changed in this release

<table id="table_vlp_vl5_zbc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table id="table_brb_jrn_xwb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addAggregate\(\)
-   addHaving\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addQuery\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setValue\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table id="table_ajg_1t5_szb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[AWA Manual Assignment API](https://www.servicenow.com/docs/access?context=awa_manual_assign-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new request body parameters. POST /awa/workitems/\{work\_item\_sys\_id\}/assignments

</td></tr><tr><td>

[Continuous Integration/Continuous Delivery \(CICD\) API](https://www.servicenow.com/docs/access?context=cicd-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new optional query parameters for specifying whether to run a test suite as a performance test and in Cloud Runner. POST /sn\_cicd/testsuite/run

</td></tr></tbody>
</table><table id="table_ert_xdv_dcc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

V1.3.1

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

The LeadtoCashCore script include is enhanced to support reconfiguration use cases:-   createInstance\(\) - Returns **\_state** identifying whether the entity record is in an active or inactive state.
-   delta\(\) - **additionalParams** now supports the ability to ignore attributes to compare in source and dirtyJSONs.
-   effect\(\) - **additionalParams** now supports the ability to provide context variable keys instead of dictionary field names. Additionally, effect\(\) returns the **\_state** parameter identifying whether the entity record is in an active or inactive state.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

V2.0.0

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

commitInstance\(\) now returns the dataObject object which displays the status of an asynchronous transaction for users to review and submit the transaction for further fulfillment.

</td></tr></tbody>
</table><table id="table_n4j_mxv_lbc"><thead><tr><th>

 

</th><th>

 

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

CSM Openframe

</td><td>

V1.0

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added **workitem\_rejected** and **workitem\_accepted** response payloads.subscribe\(\)

</td></tr><tr><td>

CSM Openframe

</td><td>

V1.1

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added **isAutoAccepted** flag in response payloads.subscribe\(\)

</td></tr></tbody>
</table><table id="table_nq4_nxv_lbc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Customer Contracts and Entitlements

</td><td>

V4.0

</td><td>

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_pss\_core/servicecontract/\{id\}
-   GET /sn\_pss\_core/servicecontract/contractline/\{id\}
-   POST /sn\_pss\_core/servicecontract
-   POST /sn\_pss\_core/servicecontract/contractline

</td></tr><tr><td>

Entitlements Verification

</td><td>

V2.0

</td><td>

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_ent\_verify/verifyentitlements
-   GET /sn\_ent\_verify/verifyentitlements/getEntitlementCharacteristic/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   For all endpoints, the namespace and endpoint paths changed from sn\_ind\_tmt\_ord to sn\_tmf\_api.
-   The following methods return two new parameters, **href** and **orderDate**.
    -   GET /sn\_tmf\_api/order/serviceOrder
    -   POST /sn\_tmf\_api/order/serviceOrder/cancelserviceorder
    -   Service Order Open API – POST /sn\_tmf\_api/order/serviceOrder
    -   POST /sn\_tmf\_api/order/serviceOrder/outboundresponse

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   For all endpoints, the namespace and endpoint paths changed from sn\_ind\_tmt\_ord to sn\_tmf\_api.
-   productOffering methods return two new optional parameters, **href** and **lifecycleStatus**:
    -   GET /sn\_tmf\_api/catalogmanagement/productOffering
    -   GET /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
    -   PATCH /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
    -   POST /sn\_tmf\_api/catalogmanagement/productOffering
-   productSpecification methods return three new optional parameters, **isBundle**, **href**, and **lifecycleStatus**:
    -   GET /sn\_tmf\_api/catalogmanagement/productSpecification
    -   GET /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
    -   PATCH /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
    -   POST /sn\_tmf\_api/catalogmanagement/productSpecification

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

V3.5.0

</td><td>

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

The **sort\_by** and **sort\_direction** request body parameters are no longer supported. Observables returned in the response are sorted by **sys\_id** in ascending order.POST /sn\_sec\_tisc/threat\_intel\_data/observables

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

 

</td><td>

[WSD Extra Service Request API](https://www.servicenow.com/docs/access?context=wsd_extra_serv_req-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new request body parameter, reservationDateTimeChanged.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable API](https://www.servicenow.com/docs/access?context=wsd_reservable-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable V2 API](https://www.servicenow.com/docs/access?context=wsd_reservable-V2-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.POST /sn\_wsd\_rsv/v2/reservable/list\_reservables

</td></tr></tbody>
</table>## Activation information

The following APIs are available by default:

-   Cloud Services Catalog API
-   DynamicSchemaAPI
-   GlideAggregate
-   GlideDate
-   GlideDynamicAttributeStore
-   GlideElementAttributeStore
-   GlideRecord
-   HistoryWalker
-   NumberFormatter
-   openFrameAPI
-   PDAutomationProvider
-   PDFGenerationAPI
-   PlaybookExperience
-   Product Catalog Open API
-   Service Order Open API

The following APIs require plugin activation:

-   The Appointment Open API requires the following plugins to be activated:
    -   Appointment Booking \(com.snc.appointment\_booking\)
    -   Field Service Management \(com.snc.work\_management\)
    -   Field Service Management for Telecommunications \(com.sn\_fsmt\)
    -   Telecommunication Open APIs \(com.sn\_tmf\_api\)
-   The AWA Manual Assignment API requires the Advanced Work Assignment \(com.glide.awa\) plugin to be activated.
-   The LeadtoCashCore script include requires the Lead to Cash Core \(com.snd.l2c.core\) plugin to be activated.
-   The PersonalAuthAPI requires the Personal Authentication \(com.snc.sn\_ihub\_personal\_auth\) plugin to be activated.
-   The Proactive Engagement API requires the Proactive Engagement \(proactive-engagement\) plugin to be activated.
-   The PSBPublicAPIUtil requires the Service Exchange for Providers application \(sn\_sb\_pro\) and the Service Exchange Base \(sn\_sb\) plugins to be activated.
-   The Resource Inventory Open API requires the Customer Network Inventory Core application \(com.app-ni-core\) plugin to be activated.
-   The Service Contract API requires the following plugins to be activated:
    -   Customer Contracts and Entitlements \(com.sn\_pss\_core\)
    -   Customer Service Install Base Management \(com.snc.install\)
    -   Product Catalog Management Core \(com.sn\_prd\)
-   The Service Test Management Open API requires the Customer Service Problem Management \(com.sn\_sprb\_mgmt\) plugin to be activated.
-   The Verify Entitlements API requires the Entitlement Verification \(sn\_ent\_verify\) plugin to be activated.
-   The WSD Extra Service Request API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.
-   The WSD Reservable API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.
-   The WSD Reservable V2 API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

