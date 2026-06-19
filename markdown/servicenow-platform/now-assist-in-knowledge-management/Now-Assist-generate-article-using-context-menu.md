---
title: Edit an article using the Now Assist context menu
description: Elaborate or shorten content within a Knowledge article using the Now Assist context menu feature that enables agents to leverage the generative AI capabilities of Now Assist in Knowledge Management.The Now Assist Knowledge content recommendation skill currently supports only a limited set of HTML tags and styles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-generate-article-using-context-menu.html
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, AI Search, Configuring Now Assist, Now LLM, large language model, Knowledge content recommendation, Context menu, Now Assist, Gen AI, Generative AI, AI Search, Configuring Now Assist, Now LLM, large language model, Knowledge content recommendation, Context menu]
breadcrumb: [Use Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit an article using the Now Assist context menu

Elaborate or shorten content within a Knowledge article using the Now Assist context menu feature that enables agents to leverage the generative AI capabilities of Now Assist in Knowledge Management.

## Before you begin

The Now Assist Knowledge content recommendation skill required to enable the context menu feature is activated by the admin. To configure the skill see [Configure skill for Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-configuring-context-menu-skill.md) the elaborate and shorten function of the context menu feature is available for all article templates.

Role required: author or agent

## Procedure

1.  Open a Knowledge article or create a new one.

2.  Select the content that you want to elaborate or shorten from any of the fields in the form.

    \[Omitted image "NA-elaborate-shorten-content-1.png"\] Alt text: Use Now Assist to Elaborate or shorten content in the Knowledge article.

3.  Select the Now Assist icon \[Omitted image "Now\_Assist\_icon.png"\] Alt text: Now Assist icon and select either **Elaborate** or **Shorten** from the context menu. \[Omitted image "NA-elaborate-shorten-content-2.png"\] Alt text: Now Assist elaborates content in a Knowledge article to make it descriptive.

    \[Omitted image "NA-elaborate-shorten-content-2.png"\] Alt text: Now Assist elaborates content in a Knowledge article to make it descriptive.

4.  Select **Insert** to add the Now Assist generated content to the article.


**Parent Topic:**[Using Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/using-now-assist-in-km.md)

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


