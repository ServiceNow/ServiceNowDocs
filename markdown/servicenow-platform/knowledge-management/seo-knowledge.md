---
title: SEO for canonical URLs and localized versions of knowledge articles
description: Improve the searchability of knowledge articles by adding tags for canonical URLs and hreflang tags for translated knowledge articles.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# SEO for canonical URLs and localized versions of knowledge articles

Improve the searchability of knowledge articles by adding tags for canonical URLs and **hreflang** tags for translated knowledge articles.

You can add the default tags for canonical URLs and **hreflang** tags by selecting the **Use SEO script** check box on the Knowledge Article View \[kb\_article\_view\] page record. For more information, see [Enable SEO for canonical URLs and localized versions of a portal page](https://www.servicenow.com/docs/access?context=seo-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

When the **Use SEO script** option is selected:

-   The canonical URLs for a knowledge article are added to the knowledge article view page.

    Example canonical URL: `https://<instance name>.servicenow-com/csp?id=kb_article_view&sysparm_article=<article number>`

-   The **hreflang** tags for the translated versions of a knowledge article are added to the knowledge article view page.

    Example URL with an **hreflang** tag: `<link rel=“alternate” href=“https://<instance name>.servicenow-com/csp/fr?id=kb_article_view&sysparm_article=<article number>” hreflang=“fr”`/&gt;

    **Note:** A self-referencing **hreflang** URL is also added for the language of current knowledge article.

    For example, an English knowledge article is viewed by visiting a URL with the following format:

    `https://<instance name>.servicenow-com/csp/?id=kb_article_view&sys_kb_id=<sys_id>`

    In addition to the **hreflang** tags added for translations, the English language self-referencing **hreflang** tag is added:

    `<link rel=“alternate” href=“https://<instance name>.servicenow-com/csp/?id=kb_article_view&sys_kb_id=<sys_id>” hreflang=“en”/>`


## Script includes for canonical URLs and hreflang tags

By default, the knowledge article view page uses the SPSEOHeaderTagsArticleViewSNC script include to add the SEO tags for canonical URLs and **hreflang** tags.

The following table describes the script includes for adding canonical URLs and **hreflang** tags to Service Portal pages, including the knowledge article view page.

<table id="table_pl2_qc2_dmb"><thead><tr><th>

Script include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SPSEOHeaderTagsSNC

</td><td>

Includes the default implementation for the canonical URLs and **hreflang** tags for Service Portal pages. This script include is read-only.

 For more information, see [Enable SEO for canonical URLs and localized versions of a portal page](https://www.servicenow.com/docs/access?context=seo-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

SPSEOHeaderTags

</td><td>

Facilitates overriding the default implementation in the SPSEOHeaderTagsSNC script include for Service Portal pages. The SPSEOHeaderTags script include extends the  SPSEOHeaderTagsSNC script include.

</td></tr><tr><td>

 SPSEOHeaderTagsArticleViewSNC

</td><td>

Overrides the generateHrefLangArray and generateCanonicalURL functions for the knowledge article view page configured in the SPSEOHeaderTags script include. The SPSEOHeaderTagsArticleViewSNC script include is read-only and extends the   SPSEOHeaderTags script include.

</td></tr><tr><td>

SPSEOHeaderTagsArticleView

</td><td>

Facilitates overriding the default implementation in the SPSEOHeaderTagsArticleViewSNC script include for the knowledge article view page.The SPSEOHeaderTagsArticleView extends the  SPSEOHeaderTagsArticleViewSNC script include.

</td></tr></tbody>
</table>As an administrator, you can add canonical URLs, **hreflang** tags, and any custom headers for knowledge articles by updating the SPSEOHeaderTagsArticleView script include. For more information, see [Configure custom SEO tags for canonical URLs and localized knowledge articles](../task/configure-seo-knowledge.md).

**Parent Topic:**[Knowledge Management reference](../reference/knowledge-management-reference.md)

