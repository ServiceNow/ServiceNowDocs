---
title: Combined API release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for API from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-api-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 24
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for API from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQBScopedScriptableAPI - Scoped](https://servicenow-staging.fluidtopics.net/access?context=CMDBQBScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   getSavedQueryExecutionDetails\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=NumberFormatterBoth&family=xanadu&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDAutomationProvider - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDAutomationProviderBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   activateProcess\(\)
-   deactivateProcess\(\)
-   duplicateProcess\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr><tr><td>

[PersonalAuthAPI - Scoped](https://servicenow-staging.fluidtopics.net/access?context=PersonalAuthAPIScoped&family=xanadu&ft:locale=en-US)

</td><td>

-   PersonalAuthAPI\(\)
-   getInitiatorURL\(\)
-   isTokenValid\(\)
-   revokeToken\(\)

</td></tr><tr><td>

[PlaybookExperience - Scoped](https://servicenow-staging.fluidtopics.net/access?context=PlaybookExperienceScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

restartPlaybook\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQueryBuilderAPI - Global](https://servicenow-staging.fluidtopics.net/access?context=CMDBQueryBuilderAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[DynamicSchemaAPI - Global](https://servicenow-staging.fluidtopics.net/access?context=DynamicSchemaAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   clearDynamicCategoryCache\(\)
-   clearDynamicChoiceSetCache\(\)
-   clearDynamicAttributeGroupCache\(\)
-   clearDynamicAttributeGroupCacheItem\(\)
-   clearDynamicCategoryCacheItem\(\)
-   clearDynamicChoiceSetItem\(\)
-   get\(\)

</td></tr><tr><td>

[GlideAggregate - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideAggregateAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures

</td></tr><tr><td>

[GlideDate - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDateAPI&family=xanadu&ft:locale=en-US)

</td><td>

parseDate\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttStoreAPI&family=xanadu&ft:locale=en-US)

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

[GlideElementDynamicAttributeStore - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideElementDynamicAttStoreAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeDisplayValues\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideRecordAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\) - two signatures
-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValue\(\) - two signatures
-   setDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValues\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=NumberFormatterBoth&family=xanadu&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[m\_form - Client](https://servicenow-staging.fluidtopics.net/access?context=m_formClientAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   getValue\(\)
-   setAffectedInputs\(\)
-   setValue\(\)

</td></tr><tr><td>

[MobileScriptIncludeCaller - Client](https://servicenow-staging.fluidtopics.net/access?context=MobileScriptInclCallerClientAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   MobileScriptIncludeCaller\(\)
-   addParam\(\)
-   call\(\)

</td></tr></tbody>
</table>

</td></tr><tr><td>

Yokohama

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=ConsoleAPI&family=yokohama&ft:locale=en-US)

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

[Fetch - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=FetchAPI&family=yokohama&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.HeadersAPI&family=yokohama&ft:locale=en-US)

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

[Fetch Request - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.RequestAPI&family=yokohama&ft:locale=en-US)

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

[Fetch RequestInit - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.RequestInitAPI&family=yokohama&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.ResponseAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideUser - Scoped](https://servicenow-staging.fluidtopics.net/access?context=c_GlideUserScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[OrderUtil - Scoped](https://servicenow-staging.fluidtopics.net/access?context=OrderUtilScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getStateFromOrder\(\)
-   isOrderInDraftState\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[ProcessMiningIntegrationAPI - Scoped](https://servicenow-staging.fluidtopics.net/access?context=ProcessMiningIntAPIScoped&family=yokohama&ft:locale=en-US)

</td><td>

-   createProject\(\)
-   deleteProject\(\)
-   getBreakDownStats\(\)
-   getFindings\(\)
-   getMiningStatus\(\)
-   getProject\(\)
-   scheduleMining\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_RESTMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_SOAPMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr><tr><td>

[UriMatcher - Scoped](https://servicenow-staging.fluidtopics.net/access?context=UriMatcherScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   UriMatcher\(\)
-   match\(\)

</td></tr><tr><td>

[UriMatcherResponse - Scoped](https://servicenow-staging.fluidtopics.net/access?context=UriMatcherResponseScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getErrorMessages\(\)
-   isError\(\)
-   isFragmentMatches\(\)
-   isHostMatches\(\)
-   isMatch\(\)
-   isPathMatches\(\)
-   isSchemeMatches\(\)

</td></tr><tr><td>

[v\_record - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=v_recordAPI&family=yokohama&ft:locale=en-US)

</td><td>

setLastErrorMessage\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=ConsoleAPI&family=yokohama&ft:locale=en-US)

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

[Fetch - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=FetchAPI&family=yokohama&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.HeadersAPI&family=yokohama&ft:locale=en-US)

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

[Fetch Request - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.RequestAPI&family=yokohama&ft:locale=en-US)

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

[Fetch RequestInit - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.RequestInitAPI&family=yokohama&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://servicenow-staging.fluidtopics.net/access?context=Fetch.ResponseAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideDynamicAttribute - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttributeAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttStoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

getDynamicAttributes\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideElementDynamicAttStoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getDynamicAttributesInSchema\(\)
-   getDynamicAttributesInStore\(\)

</td></tr><tr><td>

[GlideTransientDynamicAttribute - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideTransientDynamicAttributeAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideUser - Global](https://servicenow-staging.fluidtopics.net/access?context=GUserAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_RESTMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_SOAPMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[AWA Offer Work API](https://servicenow-staging.fluidtopics.net/access?context=awa-offer-work-api&family=yokohama&ft:locale=en-US)

</td><td>

POST /now/awa/documents/\{document\_table\}/\{document\_sys\_id\}/offer

</td></tr><tr><td>

[Continuous Integration and Continuous Delivery \(CICD\) Update Set API](https://servicenow-staging.fluidtopics.net/access?context=cicd-update-set-api&family=yokohama&ft:locale=en-US)

</td><td>

-   POST /sn\_cicd/update\_set/retrieve
-   POST /sn\_cicd/update\_set/commitMultiple
-   POST /sn\_cicd/update\_set/preview/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/back\_out
-   POST /sn\_cicd/update\_set/commit/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/create

</td></tr></tbody>
</table><table><thead><tr><th>

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

[LeadAPIHelperOOB - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadAPIHelperOOBAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getJSONFromGR\(\)
-   getLeadsJSON\(\)
-   getTransformedLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIProcessUtilOOB - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadAPIProcessUtilOOBAPI&family=yokohama&ft:locale=en-US)

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

[LeadAPIValidationUtilOOB - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadAPIValidationUtilOOBAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   validateLeadObjectForPatchCall\(\)
-   validateLeadObjectForPostCall\(\)

</td></tr><tr><td>

Sales and Service API Core

</td><td>

7.0.0

</td><td>

[IBQConfigBase API - Scoped](https://servicenow-staging.fluidtopics.net/access?context=IBQConfigBaseAPIBoth&family=yokohama&ft:locale=en-US)

</td><td>

-   generateParentRecord\(\)
-   getRunMode\(\)
-   processInboundQueueRequest\(\)

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[OrderGuide - Scoped](https://servicenow-staging.fluidtopics.net/access?context=OrderGuideScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

isOrderInDraftState\(\)

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|Customer Service Management|v1.2|[openFrameAPI - Client](https://servicenow-staging.fluidtopics.net/access?context=c_openFrameAPI&family=yokohama&ft:locale=en-US)|setICContext\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - Android](https://servicenow-staging.fluidtopics.net/access?context=NowChatServiceAndroidAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebService class - Android](https://servicenow-staging.fluidtopics.net/access?context=NowWebServiceAndroidAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - iOS](https://servicenow-staging.fluidtopics.net/access?context=NowChatServiceiOSAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatServiceDelegate protocol - iOS](https://servicenow-staging.fluidtopics.net/access?context=NowChatServiceDelegateiOSProtocol&family=yokohama&ft:locale=en-US)|chatService\(\_chatService: NowChatService, systemThemeDidChange traitCollection: UITraitCollection\)|
|Mobile SDK|v2.9.0|[NowWebViewController class - iOS](https://servicenow-staging.fluidtopics.net/access?context=NWebViewControlleriOSAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebViewControllerDelegate protocol - iOS](https://servicenow-staging.fluidtopics.net/access?context=NWViewControllerDelegateiOSProtocol&family=yokohama&ft:locale=en-US)|nowWebViewController\(\_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection\)|

<table><thead><tr><th>

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

[AP Invoice API](https://servicenow-staging.fluidtopics.net/access?context=ap-invoice-api&family=yokohama&ft:locale=en-US)

</td><td>

-   POST /sn\_spend\_intg/ap\_invoice/xml

</td></tr><tr><td>

Expanded Product Model and Asset Classes

</td><td>

v1.0

</td><td>

[AI Assets API](https://servicenow-staging.fluidtopics.net/access?context=ai-assets-api&family=yokohama&ft:locale=en-US)

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

[Service Contract API](https://servicenow-staging.fluidtopics.net/access?context=servicecontract-api&family=yokohama&ft:locale=en-US)

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

[Verify Entitlements API](https://servicenow-staging.fluidtopics.net/access?context=verifyentitlements-api&family=yokohama&ft:locale=en-US)

</td><td>

GET /sn\_ent\_verify/verifyentitlements

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[lead API](https://servicenow-staging.fluidtopics.net/access?context=lead-api&family=yokohama&ft:locale=en-US)

</td><td>

-   GET /sn\_lead\_mgmt\_core/lead
-   GET /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}
-   POST /sn\_lead\_mgmt\_core/lead

</td></tr><tr><td>

Sales and Order Management

</td><td>

v4.0

</td><td>

[Sales Agreement API](https://servicenow-staging.fluidtopics.net/access?context=sales_agreement-api&family=yokohama&ft:locale=en-US)

</td><td>

-   GET /sn\_sales\_agmt\_core/salesagreement /\{id\}
-   POST /sn\_sales\_agmt\_core/salesagreement 

</td></tr></tbody>
</table>

</td></tr><tr><td>

Zurich

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideCurrencyCode - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=GlideCurrencyCodeBothAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getCurrencyCode\(\)
-   getNumericCurrencyCode\(\)

</td></tr><tr><td>

[GlideCurrencySymbol - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=GlideCurrencySymbolBothAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getCurrencySymbol\(\)
-   getSortedActiveCurrencySymbols\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideRecordAPI&family=zurich&ft:locale=en-US)

</td><td>

addUserQuery\(\)

</td></tr><tr><td>

[GlideSysAttachment - Scoped](https://servicenow-staging.fluidtopics.net/access?context=c_GlideSysAttachmentScopedAPI&family=zurich&ft:locale=en-US)

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

[GlideSystem - Scoped](https://servicenow-staging.fluidtopics.net/access?context=c_GlideSystemScopedAPI&family=zurich&ft:locale=en-US)

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

[GlideDynamicAttribute - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New method getNamespaceName\(\).

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttStoreAPI&family=zurich&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New methods:

-   getDynamicNamespace\(\)
-   setDynamicNamespace\(\)

</td></tr><tr><td>

[GlideDynamicNamespace - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicNamespaceAPI&family=zurich&ft:locale=en-US)

</td><td>

-   getName\(\)
-   isActive\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideRecordAPI&family=zurich&ft:locale=en-US)

</td><td>

addUserQuery\(\)

</td></tr><tr><td>

[GlideSysAttachment - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideSysAttachmentGlobalAPI&family=zurich&ft:locale=en-US)

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

[GlideSystem - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideSystemAPI&family=zurich&ft:locale=en-US)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)

</td></tr><tr><td>

[Message - Global](https://servicenow-staging.fluidtopics.net/access?context=sn_i18n.messageAPI&family=zurich&ft:locale=en-US)

</td><td>

Retrieves localized messages from the Message \[sys\_ui\_message\] table. It supports internationalization \(i18n\) by dynamically fetching messages based on the user's session language or a specified language parameter.-   getMessage\(\)
-   getMessageLang\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://servicenow-staging.fluidtopics.net/access?context=c_GlideFormAPI&family=zurich&ft:locale=en-US)

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

[GlideModal \(Next Experience\) - Client](https://servicenow-staging.fluidtopics.net/access?context=GModClientAPINX&family=zurich&ft:locale=en-US)

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

[GlideNavigation \(Next Experience\) - Client](https://servicenow-staging.fluidtopics.net/access?context=GlideNavigationClientAPINX&family=zurich&ft:locale=en-US)

</td><td>

refreshNavigator\(\)

</td></tr><tr><td>

[StopWatch \(Next Experience\) - Client](https://servicenow-staging.fluidtopics.net/access?context=StopWatchAPINX&family=zurich&ft:locale=en-US)

</td><td>

-   StopWatch\(\)
-   getTime\(\)
-   restart\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://servicenow-staging.fluidtopics.net/access?context=GlideFormAPINX&family=zurich&ft:locale=en-US)

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

[GlideUser \(Next Experience\) - Client](https://servicenow-staging.fluidtopics.net/access?context=GlideUserAPINX&family=zurich&ft:locale=en-US)

</td><td>

getRoles\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Conversation Member API](https://servicenow-staging.fluidtopics.net/access?context=conversation-member-api&family=zurich&ft:locale=en-US)

</td><td>

-   PUT now/conversation/member/\{user\_id\}/drop
-   PUT now/conversation/member/\{user\_id\}/update

</td></tr><tr><td>

[Omnichannel Callback API](https://servicenow-staging.fluidtopics.net/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

[CSM Pricing API](https://servicenow-staging.fluidtopics.net/access?context=csm-pricing-api&family=zurich&ft:locale=en-US)

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

[Omnichannel Callback API](https://servicenow-staging.fluidtopics.net/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

</td><td>

Added new endpoints, /get and /close, for retrieving and closing a given callback record. The third endpoint, /actions, allows you to perform create, update, close, and cancel operations for a callback in an external, third party system with routing capabilities.

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

[External ID Mapping API](https://servicenow-staging.fluidtopics.net/access?context=external-id-mapping-api&family=zurich&ft:locale=en-US)

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

[Digital Product Release API](https://servicenow-staging.fluidtopics.net/access?context=digital-product-release-api&family=zurich&ft:locale=en-US)

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

[TISC TAXII Server API](https://servicenow-staging.fluidtopics.net/access?context=taxii-server-api&family=zurich&ft:locale=en-US)

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

[Party Management Open API](https://servicenow-staging.fluidtopics.net/access?context=tmf-party-management-open-api&family=zurich&ft:locale=en-US)

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

[Product Inventory Open API](https://servicenow-staging.fluidtopics.net/access?context=product-inventory-open-api&family=zurich&ft:locale=en-US)

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

[Service Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=service-catalog-open-api&family=zurich&ft:locale=en-US)

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

[TISC Intel Exchange API](https://servicenow-staging.fluidtopics.net/access?context=tisc-intel-ex-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/tisc\_intel\_sharing\_api/post\_intel

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC RPZ API](https://servicenow-staging.fluidtopics.net/access?context=tisc-rpz-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/rpz\_export

</td></tr><tr><td>

Network Inventory Advanced

</td><td>

10.0

</td><td>

2025-08

</td><td>

[DCIM Metric Data Feed API](https://servicenow-staging.fluidtopics.net/access?context=dcim-metric-data-feed-api&family=zurich&ft:locale=en-US)

</td><td>

POST /api/sn\_ni\_adv/dcim/feed/\{vendorname\}

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.2

</td><td>

2025-08

</td><td>

[Omnichannel Callback API](https://servicenow-staging.fluidtopics.net/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

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

[Quote Management API](https://servicenow-staging.fluidtopics.net/access?context=quote-management-api&family=zurich&ft:locale=en-US)

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

[Work Order Management API](https://servicenow-staging.fluidtopics.net/access?context=work-order-mgmt-api&family=zurich&ft:locale=en-US)

</td><td>

-   CANCEL /sn\_tmf\_api/work\_order\_management\_api/cancelWorkOrder
-   GET /sn\_tmf\_api/work\_order\_management\_api/workordermanagement
-   GET /sn\_tmf\_api/work\_order\_management\_api/workorder/\{id\}
-   PATCH /sn\_tmf\_api/work\_order\_management\_api/workOrder/\{id\}
-   POST /sn\_tmf\_api/work\_order\_management\_api/workOrder

</td></tr></tbody>
</table>

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing API features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[HistoryWalker - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideAggregateAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addAggregate\(\)
-   addHaving\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideRecordAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addQuery\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setValue\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[AWA Manual Assignment API](https://servicenow-staging.fluidtopics.net/access?context=awa_manual_assign-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new request body parameters. POST /awa/workitems/\{work\_item\_sys\_id\}/assignments

</td></tr><tr><td>

[Continuous Integration/Continuous Delivery \(CICD\) API](https://servicenow-staging.fluidtopics.net/access?context=cicd-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new optional query parameters for specifying whether to run a test suite as a performance test and in Cloud Runner. POST /sn\_cicd/testsuite/run

</td></tr></tbody>
</table><table><thead><tr><th>

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

[LeadtoCashCore - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadToCashCoreAPI&family=xanadu&ft:locale=en-US)

</td><td>

The LeadtoCashCore script include is enhanced to support reconfiguration use cases:-   createInstance\(\) - Returns **\_state** identifying whether the entity record is in an active or inactive state.
-   delta\(\) - **additionalParams** now supports the ability to ignore attributes to compare in source and dirtyJSONs.
-   effect\(\) - **additionalParams** now supports the ability to provide context variable keys instead of dictionary field names. Additionally, effect\(\) returns the **\_state** parameter identifying whether the entity record is in an active or inactive state.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

V2.0.0

</td><td>

[LeadtoCashCore - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadToCashCoreAPI&family=xanadu&ft:locale=en-US)

</td><td>

commitInstance\(\) now returns the dataObject object which displays the status of an asynchronous transaction for users to review and submit the transaction for further fulfillment.

</td></tr></tbody>
</table><table><thead><tr><th>

 

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

[openFrameAPI - Client](https://servicenow-staging.fluidtopics.net/access?context=c_openFrameAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added **workitem\_rejected** and **workitem\_accepted** response payloads.subscribe\(\)

</td></tr><tr><td>

CSM Openframe

</td><td>

V1.1

</td><td>

[openFrameAPI - Client](https://servicenow-staging.fluidtopics.net/access?context=c_openFrameAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added **isAutoAccepted** flag in response payloads.subscribe\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

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

[Service Contract API](https://servicenow-staging.fluidtopics.net/access?context=servicecontract-api&family=xanadu&ft:locale=en-US)

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

[Verify Entitlements API](https://servicenow-staging.fluidtopics.net/access?context=verifyentitlements-api&family=xanadu&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_ent\_verify/verifyentitlements
-   GET /sn\_ent\_verify/verifyentitlements/getEntitlementCharacteristic/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Service Order Open API](https://servicenow-staging.fluidtopics.net/access?context=service-order-open-api&family=xanadu&ft:locale=en-US)

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

[Product Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-open-api&family=xanadu&ft:locale=en-US)

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

[TISC API](https://servicenow-staging.fluidtopics.net/access?context=tisc-api&family=xanadu&ft:locale=en-US)

</td><td>

The **sort\_by** and **sort\_direction** request body parameters are no longer supported. Observables returned in the response are sorted by **sys\_id** in ascending order.POST /sn\_sec\_tisc/threat\_intel\_data/observables

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

 

</td><td>

[WSD Extra Service Request API](https://servicenow-staging.fluidtopics.net/access?context=wsd_extra_serv_req-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new request body parameter, reservationDateTimeChanged.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable API](https://servicenow-staging.fluidtopics.net/access?context=wsd_reservable-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable V2 API](https://servicenow-staging.fluidtopics.net/access?context=wsd_reservable-V2-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.POST /sn\_wsd\_rsv/v2/reservable/list\_reservables

</td></tr></tbody>
</table>

</td></tr><tr><td>

Yokohama

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table>|API|Endpoints|
|---|---------|
|[Attachment API](https://servicenow-staging.fluidtopics.net/access?context=c_AttachmentAPI&family=yokohama&ft:locale=en-US)|POST /now/attachment/file: A new parameter, creation\_time, can be used to capture attachment creation times when the Now Mobile app is offline and the attachment is uploaded to a record at a later time.|

<table><thead><tr><th>

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

[LeadtoCashCore - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadToCashCoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

Enhanced the performance of the Commit Instance API to improve number generation for the number field:-   effect\(\): The **\_records\_count** return object is added to provide details about newly inserted records for a particular table, such as the table name and number of inserted records.
-   commitInstance\(\): A new additional parameter, useNumberGenerator, is added to optionally generate and apply sys\_ids to new table records in bulk.

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://servicenow-staging.fluidtopics.net/access?context=cr-TestGen-startJob_S_S_S_N_N_N_S&family=yokohama&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr></tbody>
</table><table><thead><tr><th>

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

[openFrameAPI - Client](https://servicenow-staging.fluidtopics.net/access?context=c_openFrameAPI&family=yokohama&ft:locale=en-US)

</td><td>

subscribe\(\): Added new events-   openframe\_wrap\_up\_submitted
-   openframe\_heart\_beat

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatTheme interface - Android](https://servicenow-staging.fluidtopics.net/access?context=NowChatThemeColorsAndroidInterface&family=yokohama&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebTheme interface - Android](https://servicenow-staging.fluidtopics.net/access?context=NowWebThemeAndroidInterface&family=yokohama&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatThemeable protocol - iOS](https://servicenow-staging.fluidtopics.net/access?context=NowChatThemeableiOSProtocol&family=yokohama&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebThemeable protocol - iOS](https://servicenow-staging.fluidtopics.net/access?context=NowWebThemeableiOSProtocol&family=yokohama&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr></tbody>
</table>|Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|ATF Test Generator and Cloud Runner|2.7.2|[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://servicenow-staging.fluidtopics.net/access?context=cr-TestGen-startJob_S_S_S_N_N_N_S&family=yokohama&ft:locale=en-US)|Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.|

<table><thead><tr><th>

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

[AP Invoice API](https://servicenow-staging.fluidtopics.net/access?context=ap-invoice-api&family=yokohama&ft:locale=en-US)

</td><td>

Add properties supporting bill-to address information.-   POST /sn\_spend\_intg/ap\_invoice/cxml
-   POST /sn\_spend\_intg/ap\_invoice/json

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[Cloud Runner Test Generation - POST /now/sn\_atf\_tg/test\_generation](https://servicenow-staging.fluidtopics.net/access?context=cr-TestGenAPI-POST-test-generation&family=yokohama&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr><tr><td>

Order Management

</td><td>

v11.3.0

</td><td>

[Product Order Open API](https://servicenow-staging.fluidtopics.net/access?context=tmf622_product_ordering-api&family=yokohama&ft:locale=en-US)

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

[Product Inventory Open API](https://servicenow-staging.fluidtopics.net/access?context=product-inventory-open-api&family=yokohama&ft:locale=en-US)

</td><td>

The **productSpecification** request parameter has changed from required to optional. These endpoints now retrieve all product inventory records. In prior releases, product inventory records without a specified product specification weren't returned.-   POST /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product/\{id\}

</td></tr><tr><td>

Product Catalog

</td><td>

v14.1.0

</td><td>

[Product Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-open-api&family=yokohama&ft:locale=en-US)

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
</table>

</td></tr><tr><td>

Zurich

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideSysAttachment - Scoped](https://servicenow-staging.fluidtopics.net/access?context=c_GlideSysAttachmentScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngine - Scoped](https://servicenow-staging.fluidtopics.net/access?context=IdentificationEngineScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[ProducerV2 - Scoped](https://servicenow-staging.fluidtopics.net/access?context=ProducerV2ScopedAPI&family=zurich&ft:locale=en-US)

</td><td>

send\(\) - Added a return value and error handling.

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_RESTMessageV2API&family=zurich&ft:locale=en-US)

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

[LeadtoCashCore - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadToCashCoreAPI&family=zurich&ft:locale=en-US)

</td><td>

createInstance\(\) now supports the **allowedContextTypes** parameter, enabling partial synchronization of updates or deletions for selected Related Parties back to the originating Opportunity. Previously, partial sync behavior was limited to quote line items only.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

1.6

</td><td>

2025-12

</td><td>

[LeadtoCashCore - Scoped](https://servicenow-staging.fluidtopics.net/access?context=LeadToCashCoreAPI&family=zurich&ft:locale=en-US)

</td><td>

To allow more complex business needs, getPrimitivesEPService\(\) supports the new **context.entityConfigId** parameter, which invokes createInstance\(\) script without any defined mapping using only the entity's configuration ID.

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideAggregateAPI&family=zurich&ft:locale=en-US)

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

[GlideDynamicAttribute - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US)

</td><td>

Remove support for groups in Dynamic Schema. -   getGroupName\(\)
-   getName\(\)
-   getPath\(\)
-   getType\(\)
-   isTransient\(\)

Remove getSysId\(\).

Remove GlideTransientDynamicAttribute API documentation because GlideDynamicAttribute and GlideTransientDynamicAttribute APIs provide the same solution.

</td></tr><tr><td>

[GlideRecord - Global](https://servicenow-staging.fluidtopics.net/access?context=c_GlideRecordAPI&family=zurich&ft:locale=en-US)

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

[GlideSysAttachment - Global](https://servicenow-staging.fluidtopics.net/access?context=GlideSysAttachmentGlobalAPI&family=zurich&ft:locale=en-US)

</td><td>

Support for copying any attributes from source attachment records and deleting attributes with attachments.-   copy\(\)
-   copy\(targetFieldName\)
-   copyAttachmentsByFieldNames\(\)
-   deleteAllAttachment\(\)
-   deleteAttachment\(\)

</td></tr><tr><td>

[IdentificationEngineScriptableApi - Global](https://servicenow-staging.fluidtopics.net/access?context=c_IdentEngineScriptAPI&family=zurich&ft:locale=en-US)

</td><td>

Enable the **referenceItems** properties of the incoming payload to be populated before identifying a CI using the IRE rules defined on a class.-   createOrUpdateCI\(\)
-   createOrUpdateCIEnhanced\(\)
-   identifyCIEnhanced\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://servicenow-staging.fluidtopics.net/access?context=c_RESTMessageV2API&family=zurich&ft:locale=en-US)

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

[Product Order Open API](https://servicenow-staging.fluidtopics.net/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

</td><td>

When submitting a change payload with a new or updated service location \(via **productOrderItem.product.place.id**\), the request is now processed as a move order. This means that the product order remains the same but the service is fulfilled in the new designated location.-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](https://servicenow-staging.fluidtopics.net/access?context=tmf_prod_order-PATCH-ord-productOrder-id&family=zurich&ft:locale=en-US)
-   [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}](https://servicenow-staging.fluidtopics.net/access?context=tmf_prod_order-PATCH-productorder-id&family=zurich&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://servicenow-staging.fluidtopics.net/access?context=tmf_prod_order-POST-ord-productOrder&family=zurich&ft:locale=en-US)
-   [Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder](https://servicenow-staging.fluidtopics.net/access?context=tmf_prod_order-POST-productOrder&family=zurich&ft:locale=en-US)

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2025-12

</td><td>

[Omnichannel Callback API](https://servicenow-staging.fluidtopics.net/access?context=omichannel-callback-api&family=zurich&ft:locale=en-US)

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

[Trouble Ticket Open API](https://servicenow-staging.fluidtopics.net/access?context=trouble-ticket-open-api&family=zurich&ft:locale=en-US)

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

[Product Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-open-api&family=zurich&ft:locale=en-US)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the product offering catalog.
-   **internalVersion**: Specifies the version of the product offering.
-   **prodSpecCharValueUse.​valueType**: Supports more complex product characteristic value types, like choice, checkbox, objects, and so on.
-   **version**: Specifies the external version of the product offering.

Enhanced the version and supports external system logic and complex characteristics.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=service-catalog-open-api&family=zurich&ft:locale=en-US)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the service specification.
-   **internalVersion**: Specifies the version of the service specification.
-   **specCharacteristic.valueType**: Supports more complex service characteristic value types, like choice, checkbox, objects, and so on.
-   **version**: Specifies the external version of the service specification.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Product Order Open API](https://servicenow-staging.fluidtopics.net/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the product order.
-   **internalVersion**: Specifies the version of the product specification.
-   **productOrderItem.product.productCharacteristic.valueType**: Supports more complex product characteristic value types, like choice, checkbox, objects, and so on.
-   **productOrderItem.product.productSpecification.version**: Specifies the external version of the product specification.

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Order Open API](https://servicenow-staging.fluidtopics.net/access?context=service-order-open-api&family=zurich&ft:locale=en-US)

</td><td>

Various methods are enhanced with the following parameters:-   **externalSystem**: Specifies the external system of the service order.
-   **serviceOrderItem.service.serviceCharacteristic.valueType**: Supports more complex service characteristic value types, like choice, checkbox, objects, and so on.
-   **serviceOrderItem.service.serviceSpecification.internalVersion**: Specifies the version of the service specification.
-   **serviceOrderItem.service.serviceSpecification.version**: Specifies the external version of the service specification.

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC API](https://servicenow-staging.fluidtopics.net/access?context=tisc-api&family=zurich&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/threat\_intel\_data/observables now supports filtering observables on tags and taxonomies.

</td></tr><tr><td>

Accounts Payable Invoice Processing

</td><td>

v9.5.17

</td><td>

2025-08

</td><td>

[AP Invoice API](https://servicenow-staging.fluidtopics.net/access?context=ap-invoice-api&family=zurich&ft:locale=en-US)

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

[Service Order Open API](https://servicenow-staging.fluidtopics.net/access?context=service-order-open-api&family=zurich&ft:locale=en-US)

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

[Product Catalog Open API](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-open-api&family=zurich&ft:locale=en-US)

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

[Product Inventory Open API](https://servicenow-staging.fluidtopics.net/access?context=product-inventory-open-api&family=zurich&ft:locale=en-US)

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

[Product Order Open API](https://servicenow-staging.fluidtopics.net/access?context=tmf622_product_ordering-api&family=zurich&ft:locale=en-US)

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

[Virtual Agent Bot Integration API](https://servicenow-staging.fluidtopics.net/access?context=bot-api&family=zurich&ft:locale=en-US)

</td><td>

New options for the **action** request body parameter with corresponding examples.POST /sn\_va\_as\_service/bot/integration

</td></tr></tbody>
</table>

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some API features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some API features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   The GlideEncrypter API no longer supports Triple Data Encryption Standard \(3DES\) due to updated [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) guidelines.
    -   For existing instances that upgrade to the Zurich release, the GlideEncrypter API is available for use but has been updated to automatically use the Key Management Framework algorithm. See [GlideEncrypter - Global \(deprecated\)](https://servicenow-staging.fluidtopics.net/access?context=GlideEncrypterAPI&family=zurich&ft:locale=en-US) for more information on how to continue calling this API.
    -   For all new instances created starting with the Zurich release, the GlideEncrypter API is no longer supported. Directly use the [Key Management Framework](https://servicenow-staging.fluidtopics.net/access?context=encryption&family=zurich&ft:locale=en-US) instead for all cryptography operations.
-   Dynamic groups have been removed from dynamic schema in Core Platform. For dynamic attributes defined with an associated dynamic attribute group before the Zurich release, the [GlideDynamicAttribute](https://servicenow-staging.fluidtopics.net/access?context=GlideDynamicAttributeAPI&family=zurich&ft:locale=en-US) getGroupName\(\) method originally designed for dynamic attribute groups continues to work for backwards compatibility.

The getGroupName\(\) method returns null for migrated attributes and newly created attributes.

Customers are urged to migrate to the current [Dynamic Attribute](https://servicenow-staging.fluidtopics.net/access?context=working-with-dynamic-schema&family=zurich&ft:locale=en-US) definitions to take advantage of future improvements in features and functionality. For migration details, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

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

</td></tr><tr><td>

Yokohama

</td><td>

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

</td></tr><tr><td>

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
-   GlideRecord
-   GlideSysAttachment
-   GlideUser \(Next Experience\)
-   StopWatch \(Next Experience\)

 The following APIs require plugin activation:

-   ProducerV2 requires the ServiceNow Stream Connect Installer plugin \(com.glide.hub.stream\_connect.installer\).
-   Product Order Open API requires the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin.
-   Service Order Open API requires the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin.
-   The Omnichannel Callback API requires the Omnichannel Callback \(omnichannel\_callback plugin\) plugin.
-   Party Management Open API requires the Telecommunications Open APIs \(sn\_tmf\_api\) and Customer Service Management \(com.sn\_customerservice\) plugins.
-   The sn\_erp\_integration API requires the Zero Copy Connector for ERP \(com.sn\_erp\_integration\) plugin.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

 See [API implementation and reference](https://servicenow-staging.fluidtopics.net/access?context=api-implementation-reference&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

 See [API implementation and reference](https://servicenow-staging.fluidtopics.net/access?context=api-implementation-reference&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

 See [API implementation and reference](https://servicenow-staging.fluidtopics.net/access?context=api-implementation-reference&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

