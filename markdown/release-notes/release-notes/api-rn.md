---
title: API release notes
description: ServiceNow APIs let you build custom applications and experiences. APIs were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# API release notes

ServiceNow® APIs let you build custom applications and experiences. APIs were enhanced and updated in the Yokohama release.

## API highlights for the Yokohama release

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) for more information.

## New in the Yokohama release

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   error\(\)
-   group\(\)
-   groupCollapsedString\(\)
-   groupEnd\(\)
-   info\(\)
-   log\(\)
-   table\(\)
-   time\(\)
-   timeEnd\(\)
-   timeLog\(\)
-   trace\(\)
-   warn\(\)

</td></tr><tr><td>

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Headers\(\)
-   append\(\)
-   delete\(\)
-   entries\(\)
-   forEach\(\)
-   get\(\)
-   getSetCookie\(\)
-   has\(\)
-   keys\(\)
-   set\(\)
-   values\(\)

</td></tr><tr><td>

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Request\(\)
-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   clone\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideUser - Scoped](https://www.servicenow.com/docs/access?context=c_GlideUserScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[OrderUtil - Scoped](https://www.servicenow.com/docs/access?context=OrderUtilScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getStateFromOrder\(\)
-   isOrderInDraftState\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[ProcessMiningIntegrationAPI - Scoped](https://www.servicenow.com/docs/access?context=ProcessMiningIntAPIScoped&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   createProject\(\)
-   deleteProject\(\)
-   getBreakDownStats\(\)
-   getFindings\(\)
-   getMiningStatus\(\)
-   getProject\(\)
-   scheduleMining\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr><tr><td>

[UriMatcher - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   UriMatcher\(\)
-   match\(\)

</td></tr><tr><td>

[UriMatcherResponse - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherResponseScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getErrorMessages\(\)
-   isError\(\)
-   isFragmentMatches\(\)
-   isHostMatches\(\)
-   isMatch\(\)
-   isPathMatches\(\)
-   isSchemeMatches\(\)

</td></tr><tr><td>

[v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setLastErrorMessage\(\)

</td></tr></tbody>
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   error\(\)
-   group\(\)
-   groupCollapsedString\(\)
-   groupEnd\(\)
-   info\(\)
-   log\(\)
-   table\(\)
-   time\(\)
-   timeEnd\(\)
-   timeLog\(\)
-   trace\(\)
-   warn\(\)

</td></tr><tr><td>

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Headers\(\)
-   append\(\)
-   delete\(\)
-   entries\(\)
-   forEach\(\)
-   get\(\)
-   getSetCookie\(\)
-   has\(\)
-   keys\(\)
-   set\(\)
-   values\(\)

</td></tr><tr><td>

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   Request\(\)
-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   clone\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

getDynamicAttributes\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributesInSchema\(\)
-   getDynamicAttributesInStore\(\)

</td></tr><tr><td>

[GlideTransientDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideTransientDynamicAttributeAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideUser - Global](https://www.servicenow.com/docs/access?context=GUserAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr></tbody>
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[AWA Offer Work API](https://www.servicenow.com/docs/access?context=awa-offer-work-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

POST /now/awa/documents/\{document\_table\}/\{document\_sys\_id\}/offer

</td></tr><tr><td>

[Continuous Integration and Continuous Delivery \(CICD\) Update Set API](https://www.servicenow.com/docs/access?context=cicd-update-set-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_cicd/update\_set/retrieve
-   POST /sn\_cicd/update\_set/commitMultiple
-   POST /sn\_cicd/update\_set/preview/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/back\_out
-   POST /sn\_cicd/update\_set/commit/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/create

</td></tr></tbody>
</table><table id="table_x3d_kjc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIHelperOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIHelperOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   getJSONFromGR\(\)
-   getLeadsJSON\(\)
-   getTransformedLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIProcessUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIProcessUtilOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   processCreateLead\(\)
-   processGetAllLeads\(\)
-   processGrtLeadById\(\)
-   processUpdateLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIValidationUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIValidationUtilOOBAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   validateLeadObjectForPatchCall\(\)
-   validateLeadObjectForPostCall\(\)

</td></tr><tr><td>

Sales and Service API Core

</td><td>

7.0.0

</td><td>

[IBQConfigBase API - Scoped](https://www.servicenow.com/docs/access?context=IBQConfigBaseAPIBoth&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   generateParentRecord\(\)
-   getRunMode\(\)
-   processInboundQueueRequest\(\)

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[OrderGuide - Scoped](https://www.servicenow.com/docs/access?context=OrderGuideScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

isOrderInDraftState\(\)

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|Customer Service Management|v1.2|[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|setICContext\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - Android](https://www.servicenow.com/docs/access?context=NowChatServiceAndroidAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebService class - Android](https://www.servicenow.com/docs/access?context=NowWebServiceAndroidAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceiOSAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatServiceDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceDelegateiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|chatService\(\_chatService: NowChatService, systemThemeDidChange traitCollection: UITraitCollection\)|
|Mobile SDK|v2.9.0|[NowWebViewController class - iOS](https://www.servicenow.com/docs/access?context=NWebViewControlleriOSAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebViewControllerDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NWViewControllerDelegateiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|nowWebViewController\(\_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection\)|

<table id="table_qlh_nlc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Accounts Payable Operations

</td><td>

v2.0.0

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_spend\_intg/ap\_invoice/xml

</td></tr><tr><td>

Expanded Product Model and Asset Classes

</td><td>

v1.0

</td><td>

[AI Assets API](https://www.servicenow.com/docs/access?context=ai-assets-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_ent/asset/ai\_dataset/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_model/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_prompt/\{sys\_id\}
-   GET /sn\_ent/asset/ai\_system/\{sys\_id\}
-   POST /sn\_ent/asset/ai\_dataset
-   POST sn\_ent/asset/ai\_model
-   POST /sn\_ent/asset/ai\_prompt
-   POST /sn\_ent/asset/ai\_system
-   PUT /sn\_ent/asset/ai\_dataset/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_model/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_prompt/\{sys\_id\}
-   PUT /sn\_ent/asset/ai\_system/\{sys\_id\}

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

v6.0

</td><td>

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   POST /sn\_pss\_core/servicecontract
-   GET /sn\_pss\_core/servicecontract/\{id\}
-   POST /sn\_pss\_core/servicecontract/contractline
-   GET /sn\_pss\_core/servicecontract/contractline/\{id\}

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

v6.0

</td><td>

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

GET /sn\_ent\_verify/verifyentitlements

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[lead API](https://www.servicenow.com/docs/access?context=lead-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_lead\_mgmt\_core/lead
-   GET /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   POST /sn\_lead\_mgmt\_core/lead

</td></tr><tr><td>

Sales Customer Relationship Management

</td><td>

v4.0

</td><td>

[Sales Agreement API](https://www.servicenow.com/docs/access?context=sales_agreement-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_sales\_agmt\_core/salesagreement /\{id\}
-   POST /sn\_sales\_agmt\_core/salesagreement 

</td></tr></tbody>
</table>## Changed in this release

<table id="table_x1g_1mc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table><table id="table_omt_fmc_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table>|API|Endpoints|
|---|---------|
|[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|POST /now/attachment/file: A new parameter, creation\_time, can be used to capture attachment creation times when the Now Mobile app is offline and the attachment is uploaded to a record at a later time.|

<table id="table_lcr_kmc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

V1.4

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Enhanced the performance of the Commit Instance API to improve number generation for the number field:-   effect\(\): The **\_records\_count** return object is added to provide details about newly inserted records for a particular table, such as the table name and number of inserted records.
-   commitInstance\(\): A new additional parameter, useNumberGenerator, is added to optionally generate and apply sys\_ids to new table records in bulk.

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://www.servicenow.com/docs/access?context=cloudrnr-TestGenerationAPI-scoped&version=yokohama&pubname=yokohama-api-reference&section=cr-TestGen-startJob_S_S_S_N_N_N_S&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr></tbody>
</table><table id="table_a2z_4yf_zdc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Customer Service Management

</td><td>

v1.2

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

subscribe\(\): Added new events-   openframe\_wrap\_up\_submitted
-   openframe\_heart\_beat

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatTheme interface - Android](https://www.servicenow.com/docs/access?context=NowChatThemeColorsAndroidInterface&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebTheme interface - Android](https://www.servicenow.com/docs/access?context=NowWebThemeAndroidInterface&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatThemeable protocol - iOS](https://www.servicenow.com/docs/access?context=NowChatThemeableiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebThemeable protocol - iOS](https://www.servicenow.com/docs/access?context=NowWebThemeableiOSProtocol&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|ATF Test Generator and Cloud Runner|2.7.2|[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://www.servicenow.com/docs/access?context=cloudrnr-TestGenerationAPI-scoped&version=yokohama&pubname=yokohama-api-reference&section=cr-TestGen-startJob_S_S_S_N_N_N_S&ft:locale=en-US)|Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.|

<table id="table_nbf_qmc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Accounts Payable Operations

</td><td>

v2.0.0

</td><td>

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

Add properties supporting bill-to address information.-   POST /sn\_spend\_intg/ap\_invoice/cxml
-   POST /sn\_spend\_intg/ap\_invoice/json

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[Cloud Runner Test Generation - POST /now/sn\_atf\_tg/test\_generation](https://www.servicenow.com/docs/access?context=cloudrunner-testgeneration-api&version=yokohama&pubname=yokohama-api-reference&section=cr-TestGenAPI-POST-test-generation&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr><tr><td>

Order Management

</td><td>

v11.3.0

</td><td>

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

The **productSpecification** request parameter has changed from required to optional.-   PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}
-   PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}
-   POST /sn\_ind\_tmt\_orm/order/productOrder
-   POST /sn\_ind\_tmt\_orm/productorder

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

The **productSpecification** request parameter has changed from required to optional. These endpoints now retrieve all product inventory records. In prior releases, product inventory records without a specified product specification weren't returned.-   POST /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product/\{id\}

</td></tr><tr><td>

Product Catalog

</td><td>

v14.1.0

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

</td><td>

The ability to specify product bundles has been added to the following endpoints:-   GET /sn\_tmf\_api/ catalogmanagement/catalog
-   GET /sn\_tmf\_api/ catalogmanagement/catalog/\{id\}
-   GET /sn\_tmf\_api/ catalogmanagement/productOffering
-   GET /sn\_tmf\_api/ catalogmanagement/productOffering/\{id\}
-   PATCH /sn\_tmf\_api/ catalogmanagement/productOffering/\{id\}
-   POST /sn\_tmf\_api/ catalogmanagement/productOffering
-   GET /sn\_tmf\_api/ catalogmanagement/productSpecification
-   GET/sn\_tmf\_api/ catalogmanagement/productSpecification/\{id\}
-   PATCH /sn\_tmf\_api/ catalogmanagement/productSpecification/\{id\}
-   POST /sn\_tmf\_api/ catalogmanagement/productSpecification

</td></tr></tbody>
</table>## Activation information

The following APIs are available by default:

-   Attachment
-   Console
-   Fetch
-   Fetch.Headers
-   Fetch.Request
-   Fetch.Response
-   Fetch.RequestInit
-   GlideDynamicAttribute
-   GlideDynamicAttributeStore
-   GlideElementDynamicAttributeStore
-   GlideTransientDynamicAttribute
-   GlideUser
-   openFrameAPI
-   PDFGenerationAPI
-   RESTMessageV2
-   ScriptableUriMatcher
-   SOAPMessageV2
-   UriMatcher
-   UriMatcherResponse

The following APIs require plugin activation:

-   The AI Asset API requires the Asset Classes \(sn\_ent\) plugin to be activated.
-   The AP Invoice API requires the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) plugin to be activated.
-   The AWA Offer Work API requires the Advanced Work Assignment \(com.glide.awa\) plugin to be activated.
-   The IBQConfigBase API requires the Sales and Service API Core \(com.sn\_tmt\_core\) plugin to be activated.
-   The lead API requires the Lead Management Data Model \(sn\_lead\_mgmt\_core\) plugin to be activated.
-   The Mobile SDK requires the Mobile SDK Android library \(NowSDK\) or the Mobile SDK iOS library to be downloaded and installed.
-   The openFrame API requires the com.sn\_openframe\_store plugin to be activated.
-   The OrderUtil API \(script include\) requires the Order Management \(com.sn\_ind\_tmt\_orm\) plugin to be activated.
-   The ProcessMiningIntegrationAPI requires the Process Mining Core \(com.sn\_process\_optimization\) plugin to be activated.
-   The Product Order Open and the Product Inventory Open APIs require Order Management \(sn\_ind\_tmt\_orm\) plugin to be activated.
-   The Sales Agreement API requires the following plugins to be activated:
    -   Sales Agreement Data Model \(com.sn\_sales\_agmt\_core\) 
    -   Product Catalog Management Core \(com.sn\_prd\_pm\)
    -   Pricing \(com.sn\_csm\_pricing\)  
-   The Service Contract API requires the following plugins to be activated:
    -   Customer Contracts and Entitlements \(com.sn\_pss\_core\)
    -   Customer Service Install Base Management \(com.snc.install\)
    -   Product Catalog Management Core \(com.sn\_prd\)
-   The v\_record API requires the Remote Tables \(com.glide.script.vtable\) plugin to be activated.
-   The Verify Entitlements API requires the Entitlement Verification \(com.sn\_ent\_verify\) plugin to be activated.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

