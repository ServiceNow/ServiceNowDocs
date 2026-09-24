---
title: Combined API release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for API from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-api-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 23
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for API from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

Xanadu

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQBScopedScriptableAPI - Scoped](https://www.servicenow.com/docs/access?context=CMDBQBScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   getSavedQueryExecutionDetails\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&family=xanadu&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDAutomationProvider - Scoped, Global](https://www.servicenow.com/docs/access?context=PDAutomationProviderBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   activateProcess\(\)
-   deactivateProcess\(\)
-   duplicateProcess\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr><tr><td>

[PersonalAuthAPI - Scoped](https://www.servicenow.com/docs/access?context=PersonalAuthAPIScoped&family=xanadu&ft:locale=en-US)

</td><td>

-   PersonalAuthAPI\(\)
-   getInitiatorURL\(\)
-   isTokenValid\(\)
-   revokeToken\(\)

</td></tr><tr><td>

[PlaybookExperience - Scoped](https://www.servicenow.com/docs/access?context=PlaybookExperienceScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

restartPlaybook\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CMDBQueryBuilderAPI - Global](https://www.servicenow.com/docs/access?context=CMDBQueryBuilderAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   createReport\(\)
-   deleteQuery\(\)
-   saveQuery\(\)
-   updateQuery\(\)

</td></tr><tr><td>

[DynamicSchemaAPI - Global](https://www.servicenow.com/docs/access?context=DynamicSchemaAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   clearDynamicCategoryCache\(\)
-   clearDynamicChoiceSetCache\(\)
-   clearDynamicAttributeGroupCache\(\)
-   clearDynamicAttributeGroupCacheItem\(\)
-   clearDynamicCategoryCacheItem\(\)
-   clearDynamicChoiceSetItem\(\)
-   get\(\)

</td></tr><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&family=xanadu&ft:locale=en-US)

</td><td>

parseDate\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&family=xanadu&ft:locale=en-US)

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

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeDisplayValues\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   getDynamicAttribute\(\) - two signatures
-   getDynamicAttributeValue\(\) - two signatures
-   getDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValue\(\) - two signatures
-   setDynamicAttributeDisplayValue\(\) - two signatures
-   setDynamicAttributeValues\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

walkTo\(checkpoint\)

</td></tr><tr><td>

[NumberFormatter - Scoped, Global](https://www.servicenow.com/docs/access?context=NumberFormatterBoth&family=xanadu&ft:locale=en-US)

</td><td>

-   parseWithLocale\(\)
-   parseWithSeparators\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=xanadu&ft:locale=en-US)

</td><td>

redact\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[m\_form - Client](https://www.servicenow.com/docs/access?context=m_formClientAPI&family=xanadu&ft:locale=en-US)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   getValue\(\)
-   setAffectedInputs\(\)
-   setValue\(\)

</td></tr><tr><td>

[MobileScriptIncludeCaller - Client](https://www.servicenow.com/docs/access?context=MobileScriptInclCallerClientAPI&family=xanadu&ft:locale=en-US)

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

[LeadAPIHelperOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIHelperOOBAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getJSONFromGR\(\)
-   getLeadsJSON\(\)
-   getTransformedLead\(\)

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[LeadAPIProcessUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIProcessUtilOOBAPI&family=yokohama&ft:locale=en-US)

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

[LeadAPIValidationUtilOOB - Scoped](https://www.servicenow.com/docs/access?context=LeadAPIValidationUtilOOBAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   validateLeadObjectForPatchCall\(\)
-   validateLeadObjectForPostCall\(\)

</td></tr><tr><td>

Sales and Service API Core

</td><td>

7.0.0

</td><td>

[IBQConfigBase API - Scoped](https://www.servicenow.com/docs/access?context=IBQConfigBaseAPIBoth&family=yokohama&ft:locale=en-US)

</td><td>

-   generateParentRecord\(\)
-   getRunMode\(\)
-   processInboundQueueRequest\(\)

</td></tr><tr><td>

Order Management

</td><td>

v12.5.0

</td><td>

[OrderGuide - Scoped](https://www.servicenow.com/docs/access?context=OrderGuideScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

isOrderInDraftState\(\)

</td></tr></tbody>
</table> |Application|App Version|Class|Methods|
|-----------|-----------|-----|-------|
|Customer Service Management|v1.2|[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=yokohama&ft:locale=en-US)|setICContext\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - Android](https://www.servicenow.com/docs/access?context=NowChatServiceAndroidAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebService class - Android](https://www.servicenow.com/docs/access?context=NowWebServiceAndroidAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatService class - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceiOSAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowChatServiceDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NowChatServiceDelegateiOSProtocol&family=yokohama&ft:locale=en-US)|chatService\(\_chatService: NowChatService, systemThemeDidChange traitCollection: UITraitCollection\)|
|Mobile SDK|v2.9.0|[NowWebViewController class - iOS](https://www.servicenow.com/docs/access?context=NWebViewControlleriOSAPI&family=yokohama&ft:locale=en-US)|updateTheme\(\)|
|Mobile SDK|v2.9.0|[NowWebViewControllerDelegate protocol - iOS](https://www.servicenow.com/docs/access?context=NWViewControllerDelegateiOSProtocol&family=yokohama&ft:locale=en-US)|nowWebViewController\(\_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection\)|

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

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&family=yokohama&ft:locale=en-US)

</td><td>

-   POST /sn\_spend\_intg/ap\_invoice/xml

</td></tr><tr><td>

Expanded Product Model and Asset Classes

</td><td>

v1.0

</td><td>

[AI Assets API](https://www.servicenow.com/docs/access?context=ai-assets-api&family=yokohama&ft:locale=en-US)

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

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&family=yokohama&ft:locale=en-US)

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

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&family=yokohama&ft:locale=en-US)

</td><td>

GET /sn\_ent\_verify/verifyentitlements

</td></tr><tr><td>

Lead Management

</td><td>

v3.0

</td><td>

[lead API](https://www.servicenow.com/docs/access?context=lead-api&family=yokohama&ft:locale=en-US)

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

[Sales Agreement API](https://www.servicenow.com/docs/access?context=sales_agreement-api&family=yokohama&ft:locale=en-US)

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

Xanadu

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addAggregate\(\)
-   addHaving\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addQuery\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setValue\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[AWA Manual Assignment API](https://www.servicenow.com/docs/access?context=awa_manual_assign-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new request body parameters. POST /awa/workitems/\{work\_item\_sys\_id\}/assignments

</td></tr><tr><td>

[Continuous Integration/Continuous Delivery \(CICD\) API](https://www.servicenow.com/docs/access?context=cicd-api&family=xanadu&ft:locale=en-US)

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

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=xanadu&ft:locale=en-US)

</td><td>

The LeadtoCashCore script include is enhanced to support reconfiguration use cases:-   createInstance\(\) - Returns **\_state** identifying whether the entity record is in an active or inactive state.
-   delta\(\) - **additionalParams** now supports the ability to ignore attributes to compare in source and dirtyJSONs.
-   effect\(\) - **additionalParams** now supports the ability to provide context variable keys instead of dictionary field names. Additionally, effect\(\) returns the **\_state** parameter identifying whether the entity record is in an active or inactive state.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

V2.0.0

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=xanadu&ft:locale=en-US)

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

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=xanadu&ft:locale=en-US)

</td><td>

Added **workitem\_rejected** and **workitem\_accepted** response payloads.subscribe\(\)

</td></tr><tr><td>

CSM Openframe

</td><td>

V1.1

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=xanadu&ft:locale=en-US)

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

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&family=xanadu&ft:locale=en-US)

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

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&family=xanadu&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_ent\_verify/verifyentitlements
-   GET /sn\_ent\_verify/verifyentitlements/getEntitlementCharacteristic/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&family=xanadu&ft:locale=en-US)

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

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=xanadu&ft:locale=en-US)

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

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&family=xanadu&ft:locale=en-US)

</td><td>

The **sort\_by** and **sort\_direction** request body parameters are no longer supported. Observables returned in the response are sorted by **sys\_id** in ascending order.POST /sn\_sec\_tisc/threat\_intel\_data/observables

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

 

</td><td>

[WSD Extra Service Request API](https://www.servicenow.com/docs/access?context=wsd_extra_serv_req-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new request body parameter, reservationDateTimeChanged.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable API](https://www.servicenow.com/docs/access?context=wsd_reservable-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable V2 API](https://www.servicenow.com/docs/access?context=wsd_reservable-V2-api&family=xanadu&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.POST /sn\_wsd\_rsv/v2/reservable/list\_reservables

</td></tr></tbody>
</table>

</td></tr><tr><td>

Yokohama

</td><td>

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

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

Enhanced the performance of the Commit Instance API to improve number generation for the number field:-   effect\(\): The **\_records\_count** return object is added to provide details about newly inserted records for a particular table, such as the table name and number of inserted records.
-   commitInstance\(\): A new additional parameter, useNumberGenerator, is added to optionally generate and apply sys\_ids to new table records in bulk.

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)](https://www.servicenow.com/docs/access?context=cr-TestGen-startJob_S_S_S_N_N_N_S&family=yokohama&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr></tbody>
</table> <table><thead><tr><th>

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

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&family=yokohama&ft:locale=en-US)

</td><td>

subscribe\(\): Added new events-   openframe\_wrap\_up\_submitted
-   openframe\_heart\_beat

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatTheme interface - Android](https://www.servicenow.com/docs/access?context=NowChatThemeColorsAndroidInterface&family=yokohama&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebTheme interface - Android](https://www.servicenow.com/docs/access?context=NowWebThemeAndroidInterface&family=yokohama&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowChatThemeable protocol - iOS](https://www.servicenow.com/docs/access?context=NowChatThemeableiOSProtocol&family=yokohama&ft:locale=en-US)

</td><td>

Updated available chat UI color defaults.

</td></tr><tr><td>

Mobile SDK

</td><td>

v2.9.0

</td><td>

[NowWebThemeable protocol - iOS](https://www.servicenow.com/docs/access?context=NowWebThemeableiOSProtocol&family=yokohama&ft:locale=en-US)

</td><td>

Updated available web view UI color defaults.

</td></tr></tbody>
</table> <table><thead><tr><th>

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

[AP Invoice API](https://www.servicenow.com/docs/access?context=ap-invoice-api&family=yokohama&ft:locale=en-US)

</td><td>

Add properties supporting bill-to address information.-   POST /sn\_spend\_intg/ap\_invoice/cxml
-   POST /sn\_spend\_intg/ap\_invoice/json

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

2.7.2

</td><td>

[Cloud Runner Test Generation - POST /now/sn\_atf\_tg/test\_generation](https://www.servicenow.com/docs/access?context=cr-TestGenAPI-POST-test-generation&family=yokohama&ft:locale=en-US)

</td><td>

Added the **testSuite** parameter allowing you to set the name of the new test suite that is created during test generation.

</td></tr><tr><td>

Order Management

</td><td>

v11.3.0

</td><td>

[Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&family=yokohama&ft:locale=en-US)

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

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&family=yokohama&ft:locale=en-US)

</td><td>

The **productSpecification** request parameter has changed from required to optional. These endpoints now retrieve all product inventory records. In prior releases, product inventory records without a specified product specification weren't returned.-   POST /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product
-   GET /api/sn\_prd\_invt\_/product/\{id\}

</td></tr><tr><td>

Product Catalog

</td><td>

v14.1.0

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&family=yokohama&ft:locale=en-US)

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

-   **Activation information**

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

Xanadu

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

 See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

 See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

