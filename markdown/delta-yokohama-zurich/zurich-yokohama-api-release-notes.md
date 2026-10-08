---
title: Combined API release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for API from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-api-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined API release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for API from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family API release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading API to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Yokohama

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&family=yokohama&ft:locale=en-US)

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

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&family=yokohama&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&family=yokohama&ft:locale=en-US)

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

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&family=yokohama&ft:locale=en-US)

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

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&family=yokohama&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideUser - Scoped](https://www.servicenow.com/docs/access?context=c_GlideUserScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[OrderUtil - Scoped](https://www.servicenow.com/docs/access?context=OrderUtilScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getStateFromOrder\(\)
-   isOrderInDraftState\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[ProcessMiningIntegrationAPI - Scoped](https://www.servicenow.com/docs/access?context=ProcessMiningIntAPIScoped&family=yokohama&ft:locale=en-US)

</td><td>

-   createProject\(\)
-   deleteProject\(\)
-   getBreakDownStats\(\)
-   getFindings\(\)
-   getMiningStatus\(\)
-   getProject\(\)
-   scheduleMining\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr><tr><td>

[UriMatcher - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   UriMatcher\(\)
-   match\(\)

</td></tr><tr><td>

[UriMatcherResponse - Scoped](https://www.servicenow.com/docs/access?context=UriMatcherResponseScopedAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getErrorMessages\(\)
-   isError\(\)
-   isFragmentMatches\(\)
-   isHostMatches\(\)
-   isMatch\(\)
-   isPathMatches\(\)
-   isSchemeMatches\(\)

</td></tr><tr><td>

[v\_record - Scoped, Global](https://www.servicenow.com/docs/access?context=v_recordAPI&family=yokohama&ft:locale=en-US)

</td><td>

setLastErrorMessage\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[Console - Scoped, Global](https://www.servicenow.com/docs/access?context=ConsoleAPI&family=yokohama&ft:locale=en-US)

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

[Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&family=yokohama&ft:locale=en-US)

</td><td>

fetch\(\)

</td></tr><tr><td>

[Fetch Headers - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.HeadersAPI&family=yokohama&ft:locale=en-US)

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

[Fetch Request - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestAPI&family=yokohama&ft:locale=en-US)

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

[Fetch RequestInit - Scoped, Global](https://www.servicenow.com/docs/access?context=Fetch.RequestInitAPI&family=yokohama&ft:locale=en-US)

</td><td>

requestInit\(\)

</td></tr><tr><td>

[Fetch Response - Scoped,Global](https://www.servicenow.com/docs/access?context=Fetch.ResponseAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   arrayBuffer\(\)
-   blob\(\)
-   bytes\(\)
-   formData\(\)
-   json\(\)
-   text\(\)

</td></tr><tr><td>

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

getDynamicAttributes\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getDynamicAttributesInSchema\(\)
-   getDynamicAttributesInStore\(\)

</td></tr><tr><td>

[GlideTransientDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideTransientDynamicAttributeAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getSysId\(\)
-   getName\(\)
-   getType\(\)
-   getGroupName\(\)
-   getPath\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideUser - Global](https://www.servicenow.com/docs/access?context=GUserAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)

</td></tr><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDFAsync\(\)
-   convertToPDFWithHeaderFooterAsync\(\)

</td></tr><tr><td>

[RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

setAllowedRedirectURIs\(\)

</td></tr><tr><td>

[SOAPMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_SOAPMessageV2API&family=yokohama&ft:locale=en-US)

</td><td>

-   setAllowedRedirectURIs\(\)
-   setFollowRedirect\(\)

</td></tr></tbody>
</table><table><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[AWA Offer Work API](https://www.servicenow.com/docs/access?context=awa-offer-work-api&family=yokohama&ft:locale=en-US)

</td><td>

POST /now/awa/documents/\{document\_table\}/\{document\_sys\_id\}/offer

</td></tr><tr><td>

[Continuous Integration and Continuous Delivery \(CICD\) Update Set API](https://www.servicenow.com/docs/access?context=cicd-update-set-api&family=yokohama&ft:locale=en-US)

</td><td>

-   POST /sn\_cicd/update\_set/retrieve
-   POST /sn\_cicd/update\_set/commitMultiple
-   POST /sn\_cicd/update\_set/preview/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/back\_out
-   POST /sn\_cicd/update\_set/commit/\{remote\_update\_set\_id\}
-   POST /sn\_cicd/update\_set/create

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

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing API features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

<table><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

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

[PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&family=yokohama&ft:locale=en-US)

</td><td>

-   convertToPDF\(\)
-   convertToPDFWithHeaderFooter\(\)

 New properties, glide.pdf.url.whitelisting.enabled and com.snc.pdf.whitelisted\_urls, have been added to ensure whether external URLs provided should be rendered in the PDF output.

 A new property, accessibilityEnabled, has been added for PDF accessibility support.

</td></tr></tbody>
</table>|API|Endpoints|
|---|---------|
|[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&family=yokohama&ft:locale=en-US)|POST /now/attachment/file: A new parameter, creation\_time, can be used to capture attachment creation times when the Now Mobile app is offline and the attachment is uploaded to a record at a later time.|

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some API features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate API.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for API we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

