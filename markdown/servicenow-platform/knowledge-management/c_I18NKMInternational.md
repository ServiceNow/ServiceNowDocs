---
title: I18N - Knowledge internationalization
description: The optional knowledge internationalization features enable knowledge users to view articles in multiple languages.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# I18N - Knowledge internationalization

The optional knowledge internationalization features enable knowledge users to view articles in multiple languages.

Beginning with the San Diego release, the I18N: Knowledge Management Internationalization v2 \(com.glideapp.knowledge.i18n2\) plugin is installed when any language pack is activated. In versions prior to San Diego, this plugin was installed along with the Internationalization \(com.glide.i18n\) plugin.

Knowledge internationalization enables the knowledge management team to create language-specific knowledge articles and keep translations of the same article related to each other so they are easy to manage. Users can view and search within their own language while still being able to view articles in other languages when necessary.

## Set a custom language for the article

Beginning with the San Diego release, users with elevated privileges can add a custom language by adding language entries in the Choice \[sys\_choice\] table to display the selected article in multiple languages. On the article page, the **Language** list shows all the languages for which the article language translation is available.

## Set the search language for articles

You can set the default language for searching articles to a language different from the logged-in language by specifying the language as the value of the **glide.knowman.search.default\_language** system property. For example, if French is the logged-in language and you want to set English as the default language for searched articles, specify English in the system property. You can also switch to French in the UI to see the French articles. If the system property is not set, the logged-in language of the user is set as the default article language. For more information, see [Other knowledge properties](../reference/r_KnowledgeProperties.md#).

To enable search for different languages simultaneously, navigate to **Knowledge Administration** &gt; **Knowledge Search** &gt; **Properties** &gt; **Enable multi language search** and select the **Yes** check box. For information about performing a search on all available languages simultaneously, see [Search using Knowledge Management v3](../reference/r_KnowledgeSearch.md).

**Note:** If the **glide.knowman.search.default\_language** system property is inactive, you can search one language at a time. If the property is enabled, you can search for multiple languages simultaneously.

**Parent Topic:**[Knowledge Management](knowledge-management.md)

