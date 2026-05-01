---
title: Search using the Knowledge Management Service Portal
description: Enter one or more words in the search bar on the Knowledge Management Service Portal homepage to view all search results.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Search using the Knowledge Management Service Portal

Enter one or more words in the search bar on the Knowledge Management Service Portal homepage to view all search results.

Search results include items in which the short description, content, or attached files include the search term. By default, knowledge search results include articles, pinned articles, and social Q&amp;A.

You can also filter the search results.

## Enable multi-language search

The multi-language search facet is available when more than one supported language is enabled. All available languages are displayed in the facet and you can select which languages you want your search results to appear in. Your selection is maintained per session, but not across logins.

1.  To enable different languages, activate the I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) or activate one of the internationalization plugins for the language you require.

    **Note:** Activating internationalization plugins for any of the available languages automatically activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

2.  Navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge Search Properties** &gt; **Enable multi language search**.
3.  Select the **Yes** check box to enable the feature.

    **Note:** If this property is not enabled, you can only search for one language at a time.


## Search auto-correct feature

The Knowledge Management Service Portal homepage search tool also includes an auto-correct feature. When enabled, users can auto-correct a typing error in a search term by clicking one of the suggestions.

When a search term contains a misspelling, the search tool displays the search results page and includes one or more suggested terms at the top of the page under the heading **Did you mean**. Clicking one of these suggestions shows all the search results that match the selected term.

Users with the system administrator role can enable this feature.

1.  Navigate to **System Properties** &gt; **Text Search**.
2.  Set the following properties to **true**:
    -   Suggest alternate search spellings for knowledge or global search \(glide.ts.dym.enable\_spell\_correct\).
    -   Suggest related searches for knowledge or global search \(glide.ts.dym.enable\_chain\_suggest\).
3.  Click **Save**.

**Parent Topic:**[Configure the Knowledge Management Service Portal](../concept/knowledge-management-service-portal.md)

