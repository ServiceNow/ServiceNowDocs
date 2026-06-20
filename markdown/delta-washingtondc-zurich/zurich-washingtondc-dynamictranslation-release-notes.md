---
title: Combined Dynamic Translation release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Dynamic Translation from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-dynamictranslation-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Dynamic Translation release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Dynamic Translation from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Dynamic Translation release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Dynamic Translation to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Zurich, new features were introduced for Dynamic Translation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Exclusion Framework in Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dyn-translation-exclusion-framework&family=xanadu&ft:locale=en-US)**

Exclusion Framework enables you to prevent machine translation of certain words and terms. You can specify words, such as official product names, that you want to shield from the translation process. You can also input regex to prevent translation of patterns such as sys ids.

-   **[The flows used by default Translator Configurations are upgraded to v4](https://servicenow-staging.fluidtopics.net/access?context=migrate-v4-dynamic-translation&family=xanadu&ft:locale=en-US)**

With the Xanadu Patch 3 release, the flows used by default translator configurations are automatically upgraded to v4. If you want to use v4 flows and APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Exclusion Framework in Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dyn-translation-exclusion-framework&family=yokohama&ft:locale=en-US)**

Preserve text such as product names or technical terms during machine translation. With Exclusion Framework, you can specify words and patterns that shouldn't be translated.

-   **[The APIs used by default Translator Configurations are upgraded to v4](https://servicenow-staging.fluidtopics.net/access?context=migrate-v3-dynamic-translation&family=yokohama&ft:locale=en-US)**

The APIs used by default translator configurations are automatically upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Test Exclusion Rule](https://servicenow-staging.fluidtopics.net/access?context=dyn-translation-test-exclusion-rule&family=zurich&ft:locale=en-US)**

Use the new Test Exclusion Rule module to check your exclusion pattern in Dynamic Translation's Exclusion Framework. You can manually test either exact matches or pattern \(regex\) matches. See what your exclusion pattern matches when translating your input into target languages. When you are satisfied with your exclusion pattern, you can create an exclusion rule based on it with just one step.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Dynamic Translation features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Character maximum has increased for MS translation requests](https://servicenow-staging.fluidtopics.net/access?context=limitations-dynamic-translation&family=xanadu&ft:locale=en-US)**

For users of the Microsoft Azure Translator service: the maximum character limit for a translation request has increased to 50,000. The maximum character limit for a detection request remains 50,000.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Dynamic Translation features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is no longer available because IBM has withdrawn this translation service. For more information, see [IBM Watson Language Translator Service spoke](https://servicenow-staging.fluidtopics.net/access?context=ibm-translation-spoke&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Dynamic Translation features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   IBM has announced the deprecation of the IBM Watson Translator Service for IBM Cloud in all regions. As of June 10, 2023, the Language Translator tile will be removed from the IBM Cloud Platform for new customers; only existing customers will be able to access the product. As of June 10, 2024, the service will reach its End of Support date. As of December 10, 2024, the service will be withdrawn entirely and will no longer be available to any customers. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

</td></tr><tr><td>

Xanadu

</td><td>

With the Xanadu release, the IBM Watson Translator Service integration is no longer available in the ServiceNow® Store. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Dynamic Translation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Dynamic Translation is a ServiceNow AI Platform feature that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For details, see [Activate Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=activate-dynamic-translation&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Dynamic Translation is a ServiceNow AI Platform feature that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For details, see [Activate Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=activate-dynamic-translation&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Dynamic Translation is a ServiceNow AI Platform feature that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For details, see [Activate Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=activate-dynamic-translation&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Dynamic Translation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If any specific browser requirements were introduced or changed for Dynamic Translation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review details on accessibility information for Dynamic Translation, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Dynamic Translation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific highlight considerations for Dynamic Translation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   The IBM Watson Translator Service Spoke has announced a notice of deprecation for 2024.

 See the [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=washingtondc&ft:locale=en-US) documentation for an overview of ServiceNow® Dynamic Translation. See [IBM Watson Language Translator Service spoke](https://servicenow-staging.fluidtopics.net/access?context=ibm-translation-spoke&family=washingtondc&ft:locale=en-US) documentation for information specific to the IBM Watson Translator Service spoke.

</td></tr><tr><td>

Xanadu

</td><td>

-   Using Exclusion Framework, prevent certain words such as product names from being machine translated.
-   The IBM Watson Translator Service Spoke has been withdrawn and is no longer available.
-   The Microsoft Azure Translator service increased the maximum length of a translation request from 10,000 characters to 50,000 characters.

 See [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Preserve text, such as product names or technical terms, during machine translation with the Exclusion Framework feature.
-   The APIs used by default translator configurations are upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually.
-   The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is removed.

 See [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

With the new Test Exclusion Rule module you can check what your exclusion pattern matches during a test translation, then create an exclusion rule based on the pattern you tested.

 See [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=zurich&ft:locale=en-US) and [Exclusion Framework in Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dyn-translation-exclusion-framework&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

