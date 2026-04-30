---
title: Mobile text search
description: Find items, articles, and people by entering text in the search area.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile search, Using the mobile apps, Mobile Platform]
---

# Mobile text search

Find items, articles, and people by entering text in the search area.

Use search in the launcher screen header to quickly find information within the defined search sources while on your mobile device.

Your administrator can configure a search area within launcher screen headers and define a set of tables that can be searched through. There are two search engine types which your administrator can configure, Zing text indexing and search engine and AI Search. Zing search is available throughout all mobile platforms, whereas AI Search is available only on Now Mobile. For details on how an administrator can configure this features, see [Enable global search in your screen launcher](../task/sg-configure-alp-search.md).

The appearance and capabilities of the Zing and AI Search results differ. You may notice this difference as admins can configure the different search engines on different launcher screens throughout a single instance.

<table id="table_arb_qnd_h4b"><tbody><tr><td>

![Display of Zing global search results.](../image/launcher-global-search-cropped.png "Zing (global) search results")

</td><td>

![Display of AI Search search results.](../image/launcher-ais-search.png "AI Search search results")

</td></tr></tbody>
</table>Both search engines provide search suggestions as you type. They also include navigation tab filters which streamline the results displayed to help you find your specific answer. Zing search engine is available for all mobile platforms and utilizes additional data sources not associated with AI Search, such as CMDB records. For a list of tables that AI Search doesn't support for indexing, see [ServiceNow AI Platform tables excluded from AI Search indexing](https://www.servicenow.com/docs/access?context=reference-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

AI Search has the following additional capabilities and behaviors to assist you in your search.

-   Recent and popular searches - When tapping the search bar, suggested search options display according to your personal search history and queries by all users on the instance.
-   Auto-correct typos - Misspelt words are automatically corrected. 
-   Synonym handling - The search engine is able to look for similar words entered and produce results accordingly. For example, if you enter "holiday" the AI Search also searches for "vacation".
-   Genius cards and action items - Genius result cards display the most relevant answers in an attractive visual layout. They can also contain buttons for you to perform an action.

