---
title: Generate SEO information for articles using article templates
description: Improve the searchability of knowledge articles by using the content in an article template field to generate SEO tags for articles created using that template. Search Engine Optimization \(SEO\) optimise searches in public search engine.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure knowledge article templates, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate SEO information for articles using article templates

Improve the searchability of knowledge articles by using the content in an article template field to generate SEO tags for articles created using that template. Search Engine Optimization \(SEO\) optimise searches in public search engine.

## Before you begin

Role required: knowledge\_admin or admin

## About this task

**Note:** If you are using the **Standard** article template, the content of the Text field is used to generate the tags.

You can define the number of characters to be used as tags in the **glide.knowman.seo.pages.meta\_description.length** system property.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Article Templates**.

2.  Select an article template.

3.  In the **SEO Description Tag** field, search and select an article template field.

    The content in this field is used as meta description tags to search for articles created using this article template.

4.  Click **Update**.

    **Note:** You can change which article template field is used for generating SEO. Changes are applied only to knowledge articles created or updated after the change was made. To apply the update to all existing published articles created using this template, run the Populate Meta Description on KB Articles fix script.

    ![Article template page](../image/article-template-seo-tag.png "Article template page")


**Parent Topic:**[Configure knowledge article templates](../../../configure-knowledge-article-templates.md)

