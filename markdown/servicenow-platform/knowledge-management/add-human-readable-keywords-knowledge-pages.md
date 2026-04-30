---
title: Enable Human Readable URLs for the Knowledge Article View page
description: Update a human readable URL structure in the Knowledge Article View page to improve search ranking and click-through rates.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using human readable URLs for the Knowledge article page, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable Human Readable URLs for the Knowledge Article View page

Update a human readable URL structure in the Knowledge Article View page to improve search ranking and click-through rates.

## Before you begin

Role required: admin, sp\_admin

## About this task

If you are upgrading from a release earlier than the Zurich release, you must enable the Human Readable URLs feature for the Knowledge Article View page. Beginning with the Zurich release, this feature is enabled by default.

**Note:** To disable the Human Readable URLs feature, change the **glide.service\_portal.enable\_human\_readable\_urls** system property value to false.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  On the Pages form, search for the ID `kb_article_view` and select it.

3.  In the information message on the Page form indicating that you have to change the current application to edit the record, select the word **here**.

4.  On the Knowledge Article View form, in the **Human readable url structure** field enter the `%short_descr` variable.

    **Note:** You can also create a variable to add information from various data sources. For more information, see [Add human readable keywords to page URLs](https://www.servicenow.com/docs/access?context=add-human-readable-keywords-page-urls&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

5.  Select **Update**.


## Result

The *%short\_descr* variable is added to the URL structure and will enable simpler, non-technical words in the URL.

## Knowledge Article View page with human readable keywords in the URL

The following sample URL shows the keywords from the Knowledge article KB0000007. The URL considers **en** as the preferred language and displays the Knowledge article content in the English language.

```
https://<instance>.com/kb/en/faq/what-is-a-cookie?id=kb_article_view&sysparm_article=KB0000007
```

This article URL contains the field variables, and keywords in the following table.

|Field|Variable|Keywords|
|-----|--------|--------|
|Category|%category|`faq`|
|Short description|%short\_descr|`What is a cookie?`|

**Parent Topic:**[Using human readable URLs for the Knowledge article page](../concept/human-readable-urls-km.md)

