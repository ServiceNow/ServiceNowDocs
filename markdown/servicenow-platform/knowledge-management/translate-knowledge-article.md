---
title: Translate a knowledge article from a translation task
description: Start translating articles once they are published and assigned to you for translation.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use translation management, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate a knowledge article from a translation task

Start translating articles once they are published and assigned to you for translation.

## Before you begin

-   Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\).
-   Enable the **glide.knowman.translation.enable\_translation\_task** property. For more information, see [Translation management](../concept/translation-management.md).

Role required: admin, knowledge\_admin, or knowledge

## About this task

**Note:** This procedure has been superseded by the Localization Framework. For more information see Localization Framework support for Knowledge Base. This information is provided for legacy context.

For information about how administrators configure the translation API, see DynamicTranslation API.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Translation Management** &gt; **My Assigned Tasks**.

2.  In the Knowledge Translation Tasks page, select one of the listed translation tasks assigned to you.

3.  Select **Translate**.

    The **Translate from** and **Translate to** panes are side-by-side for easy comparison, as shown in the following figure.

    ![Translate knowledge article panes.](../image/translate-to-from.png)

4.  Select **Machine translate** to automatically translate to the targeted languages.

5.  Select **Create draft article** to create a draft version of the translated article.

    If a translated article is already present for that language, a new draft version overwrites the existing translated content.

6.  Select **Publish**.

    **Note:** By default, the translated version is always created as v1.0 so that the parent version remain same for all the translated versions. For more information, see [Translated KB articles always show Parent version 1.0 regardless of version used for translation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1116153).


## Result

The newly created draft is listed in the **Translated Versions** tab.

**Parent Topic:**[Use translation management](../concept/use-translation-management.md)

