---
title: Configure custom SEO tags for canonical URLs and localized knowledge articles
description: Discover relevant knowledge articles through search engines by adding custom SEO tags for canonical URLs and hreflang tags to the knowledge article view page.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure custom SEO tags for canonical URLs and localized knowledge articles

Discover relevant knowledge articles through search engines by adding custom SEO tags for canonical URLs and **hreflang** tags to the knowledge article view page.

## Before you begin

Role required: admin

## About this task

Update the SPSEOHeaderTagsArticleView script include to add canonical URLs and**hreflang** tags to the knowledge article view page. You can also add custom header tags to the knowledge article view page by implementing the generateCustomTagsForSEO function.

**Note:** The metatags will be added to the Knowledge Article View \[kb\_article\_view\] only when viewed by the user agents mentioned in **glide.knowman.serviceportal.seo\_user\_agent** system property. For more information, see [Create and edit a page using the Service Portal Designer](https://www.servicenow.com/docs/access?context=t_ConfigureAPage&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

For information about the default behavior of canonical URLs and **hreflang** tags for the knowledge article view page, see [SEO for canonical URLs and localized versions of knowledge articles](../concept/seo-knowledge.md).

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Script Includes**.

2.  Search for `SPSEOHeaderTagsArticleView`.

3.  In the **Name** column, click the **SPSEOHeaderTagsArticleView** link.

4.  On the Script Include form, modify the functions for knowledge articles.

<table id="table_qnt_srm_plb"><thead><tr><th>

Functionality

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Return a canonical URL for a knowledge article

</td><td>

Modify the generateCanonicalURL function to return the fully qualified canonical URL of a knowledge article as a string.For example, use the following URL format for a knowledge article in the customer service portal: `"https://<instance name>.servicenow-com/csp?id=kb_article_view&sysparm_article=<article number>"`

</td></tr><tr><td>

Return an **hreflang** tag for translated versions of a knowledge article

</td><td>

Modify the generateHrefLangArray function to return an **hreflang** array for the current language and the available translations for a knowledge article.For example, use the following format for a knowledge article translated in French in the customer service portal: `[{locale:'fr', href: 'https://<instance name>.servicenow-com/csp?id=kb_article_view&sysparm_article=<article number>'`\}\]

</td></tr><tr><td>

Return a custom header for a knowledge article

</td><td>

Modify the generateCustomTagsForSEO function to return any custom header tags as an array of strings used for the knowledge article view page. For example, use the following format for a custom tag for a knowledge article: `['<meta custom-tag="" property="og:title" content="Service Portal">']`

</td></tr><tr><td>

Return a SEO optimized HTML content for SEO bots

</td><td>

Modify the generateSEOTags function to return the SEO optimized HTML content in items.customSEOHTML.

</td></tr></tbody>
</table>    For more information about configuring script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

5.  Click **Update**.


