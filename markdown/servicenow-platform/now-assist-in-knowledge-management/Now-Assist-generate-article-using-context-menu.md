---
title: Edit an article using the Now Assist context menu
description: Elaborate or shorten content within a Knowledge article using the Now Assist context menu feature that enables agents to leverage the generative AI capabilities of Now Assist in Knowledge Management.The Now Assist Knowledge content recommendation skill currently supports only a limited set of HTML tags and styles.
locale: en-US
release: yokohama
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, AI Search, Configuring Now Assist, Now LLM, large language model, Knowledge content recommendation, Context menu, Now Assist, Gen AI, Generative AI, AI Search, Configuring Now Assist, Now LLM, large language model, Knowledge content recommendation, Context menu]
breadcrumb: [Use Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit an article using the Now Assist context menu

Elaborate or shorten content within a Knowledge article using the Now Assist context menu feature that enables agents to leverage the generative AI capabilities of Now Assist in Knowledge Management.

## Before you begin

The Now Assist Knowledge content recommendation skill required to enable the context menu feature is activated by the admin. To configure the skill see [Configure skill for Now Assist context menu](Now-Assist-configuring-context-menu-skill.md). The elaborate and shorten function of the context menu feature is available for all article templates.

Starting this release, Now Assist context menu can be configured to use a third-party AI model provider to elaborate or shorten content within a Knowledge article. To configure the skill, see .

Role required: author or agent

## Procedure

1.  Open a Knowledge article or create a new one.

2.  Select the content that you want to elaborate or shorten from any of the fields in the form.

    ![Use Now Assist to Elaborate or shorten content in the Knowledge article.](../image/NA-elaborate-shorten-content-1.png)

3.  Select the Now Assist icon ![Now Assist icon](../image/Now_Assist_icon.png) and select either **Elaborate** or **Shorten** from the context menu. ![Now Assist elaborates content in a Knowledge article to make it descriptive.](../image/NA-elaborate-shorten-content-2.png)

    ![Now Assist elaborates content in a Knowledge article to make it descriptive.](../image/NA-elaborate-shorten-content-2.png)

4.  Select **Insert** to add the Now Assist generated content to the article.


**Parent Topic:**[Using Now Assist in Knowledge Management](../concept/using-now-assist-in-km.md)

## Supported tags

The Now Assist Knowledge content recommendation skill currently supports only a limited set of HTML tags and styles.

The HTML tags supported and not supported by Now Assist Knowledge content recommendation are listed in the following tables. Using the content recommendation skill on text containing unsupported tags triggers an error message and requires the author to manually update the text.

|Tags|Description|
|----|-----------|
|p|Paragraph|
|br|Line breaks|
|ol, li, ul|Ordered and unordered list|
|h1, h2, h3, h4, h5, h6|Headers \(H1 to H6\)|
|strong, em, s|Bold|
|a|Anchor \(link to URL\)|

|Tags|Description|
|----|-----------|
|img, video, audio, picture, source, iframe, embed, object|Media tags|
|table, details, summary, knowledge blocks|Other tags|

**Note:**

-   Unsupported HTML tags in the selected content trigger the following error message:

    ```
    Unsupported content such as a table, knowledge block, or media file is included in your selection. Reselect and try again.
    ```

-   Styles such as bold, italics, tables, and links may not be retained and may result in unpredictable results.


