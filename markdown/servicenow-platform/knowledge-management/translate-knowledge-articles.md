---
title: Translate multiple knowledge articles into different languages
description: Translate multiple knowledge articles to localize your content into different locales.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Bulk Translation for manual translation, Bulk Translation for knowledge articles, Use translation management, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate multiple knowledge articles into different languages

Translate multiple knowledge articles to localize your content into different locales.

## Before you begin

-   [Add a custom Localization Framework setting to enable bulk translations](conf-lf-settings-manual-translations.md).
-   [Request bulk translations for multiple knowledge articles](bulk-translations-step.md).

Role required: Localization fulfiller to fulfill translation request

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Translations** &gt; **My translation request**.

2.  On the Localization Request Items page, select the gear icon \(![Gear icon](../../../common/image/gear.png)\) to add the **Localization task** to your task list.

3.  Open any localization task.

4.  On the Localization Task page, select **Translate** in the form header.

    A two-column comparison UI page displays a **Source Language** column on the left and **Target Language** column on the right. You can set the display as follows:

    -   Select **Expand all** to expand all the groups on the comparison UI.
    -   Select **Collapse all** to collapse all the groups on the comparison UI.
    -   Select **Show groups with missing translations** to see only the groups that have missing translations when the content is translated.
5.  In the comparison UI page, copy the content from **Source Language** column and paste it in **Target Language** column.

6.  Repeat the copy and paste process for each listed article.

7.  Select **Publish Translation**.

8.  In the **Publish Translations** dialog box, select **Publish Translations**.


## Result

The selected articles are translated into the selected languages and marked as version 0.01. The articles can be accessed from the Knowledge \[kb\_knowledge\] table.

**Parent Topic:**[Use Bulk Translation for manual translation](use-bts-manual-translation.md)

