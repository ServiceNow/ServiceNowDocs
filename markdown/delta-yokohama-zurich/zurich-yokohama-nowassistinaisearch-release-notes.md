---
title: Combined Now Assist in AI Search release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Now Assist in AI Search from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-nowassistinaisearch-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Now Assist in AI Search release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Now Assist in AI Search from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist in AI Search release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist in AI Search to Zurich

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

Between your current release family and Zurich, new features were introduced for Now Assist in AI Search.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=yokohama&ft:locale=en-US)**

When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://servicenow-staging.fluidtopics.net/access?context=hybrid-search-ais&family=yokohama&ft:locale=en-US)**

Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-source-ask-now-assist-suggestions&family=yokohama&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[AI Search Genius Results widget for record producers](https://servicenow-staging.fluidtopics.net/access?context=cfg-ais-genius-results-widget&family=yokohama&ft:locale=en-US)**

Administrators can configure the AI Search Genius Results widget on record producers to enhance the user experience when creating an incident. The widget displays actionable Genius Result suggestions relevant to the user's incident description. Users can select from these Genius Result suggestions to address their own issues, or can continue with their incident submission if none of the suggestions resolve their problem.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=zurich&ft:locale=en-US)**

When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://servicenow-staging.fluidtopics.net/access?context=hybrid-search-ais&family=zurich&ft:locale=en-US)**

Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-source-ask-now-assist-suggestions&family=zurich&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist in AI Search features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://servicenow-staging.fluidtopics.net/access?context=auto-complete-suggestion-types-na-ais&family=yokohama&ft:locale=en-US)**

Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****

-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://servicenow-staging.fluidtopics.net/access?context=semantic-search-ais&family=yokohama&ft:locale=en-US)**

Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.


-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=yokohama&ft:locale=en-US)**

If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.

-   **[Now Assist Q&amp;A Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-qna-genius-results&family=yokohama&ft:locale=en-US)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=yokohama&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-catalog-ordering-gr&family=yokohama&ft:locale=en-US)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**




-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://servicenow-staging.fluidtopics.net/access?context=auto-complete-suggestion-types-na-ais&family=zurich&ft:locale=en-US)**

Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://servicenow-staging.fluidtopics.net/access?context=semantic-search-ais&family=zurich&ft:locale=en-US)**

Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.

-   **[Now Assist Q&amp;A Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-qna-genius-results&family=zurich&ft:locale=en-US)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=zurich&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-catalog-ordering-gr&family=zurich&ft:locale=en-US)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=zurich&ft:locale=en-US).

-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-content-qna-genius-results&family=zurich&ft:locale=en-US)**

If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist in AI Search features or functionality were removed.

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

Between your current release family and Zurich, some Now Assist in AI Search features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Now Assist in AI Search.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   
 

</td></tr><tr><td>

Zurich

</td><td>

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist in AI Search we have noted them here.

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

If any specific browser requirements were introduced or changed for Now Assist in AI Search we have noted them here.

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

Review details on accessibility information for Now Assist in AI Search, such as specific requirements or compliance levels.

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist in AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Now Assist in AI Search supports [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=yokohama&ft:locale=en-US) in Now Assist Genius Results. For details, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-na-gr&family=yokohama&ft:locale=en-US) and [Dynamic Translation for Now Assist Actions Genius Results](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-na-actions-gr&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Now Assist in AI Search supports [Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=zurich&ft:locale=en-US) in Now Assist Genius Results. For details, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-na-gr&family=zurich&ft:locale=en-US) and [Dynamic Translation for Now Assist Actions Genius Results](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-na-actions-gr&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist in AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

 [Yokohama Patch 6](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Increase search recall with semantic indexing of Catalog Item short descriptions.

 [Yokohama Patch 3](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers.

 Yokohama Early Availability

-   Improve incident deflection for portal users by configuring record producers to display actionable and relevant Genius Results suggestions during submission of cases, incidents, problems, and similar tasks.

 See [Now Assist in AI Search](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ais&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Improve search recall and accuracy with semantic vector indexing of Catalog Item short descriptions.
-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers

 See [Now Assist in AI Search](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ais&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

