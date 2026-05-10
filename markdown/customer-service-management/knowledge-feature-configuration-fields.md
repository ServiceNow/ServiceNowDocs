---
title: Knowledge feature configuration
description: Understand the configuration and related lists of the Knowledge feature in Engagement Messenger to configure the field values.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Engagement Messenger reference, Reference, Customer Service Management]
---

# Knowledge feature configuration

Understand the configuration and related lists of the Knowledge feature in Engagement Messenger to configure the field values.

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show articles by

</td><td>

Article category that is shown on the home page of the messenger. You can select one of the following categories:

-   Featured articles: Articles that are based on the keywords that are associated with the articles.

For information on displaying articles in the Featured content section, see [Add a knowledge article to featured content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/t_PinAnArticle.md).

-   Most viewed articles: Articles that have the highest view among the articles of your knowledge base.

 The articles shown in the messenger are from the knowledge bases that you add in the **Knowledge bases** field.

</td></tr><tr><td>

Article count

</td><td>

Number of articles that are shown on the messenger home page.

 The articles are shown based on the option that you select in the **Show articles by** field.

</td></tr><tr><td>

Knowledge Bases

</td><td>

List of knowledge bases that are associated with your messenger module. Use the Edit option \(![Lock icon.](../image/lock-icon.png)\) and search to add a knowledge base to your messenger module.

</td></tr><tr><td>

Enable copy permalink

</td><td>

Option for enabling your customer to copy the permalink of a knowledge article.

</td></tr></tbody>
</table>![Knowledge feature widget displaying a list of featured articles with the article count set to 2.](../image/em-knowledge-feature-widget.png "Knowledge feature widget")

Note the following points while you are configuring the Knowledge feature on your Engagement Messenger module:

-   To add knowledge bases to your messenger module, verify that the knowledge\_admin role is manually assigned to the user with Engagement Messenger admin \[sn\_csm\_ec.ec\_admin\] role.
-   If the knowledge base that you added to the Engagement Messenger has no articles, then the homepage of the messenger UI does not display any knowledge article widget even when you select a value for the **Show articles by** and **Article count** fields.

Note the following points regarding the live preview of Knowledge feature. However, the actual functionality of the feature is not affected when the Engagement Messenger is deployed in your website.

-   The list of articles that is shown in the messenger live preview depends on the application access that the knowledge\_admin has to the articles.

    If the knowledge\_admin does not have access to any articles, then no content is displayed in the preview. In such a case, only a title **Featured articles** or **Most viewed articles** is displayed.

-   Changing the value of the **Show articles by** field refreshes only the title and not the content in the messenger preview.

