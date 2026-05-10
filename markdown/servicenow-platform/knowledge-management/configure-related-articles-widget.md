---
title: Configure knowledge related articles widget instance options
description: Configure the Knowledge Related Articles widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of related articles mapped to an article.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure knowledge related articles widget instance options

Configure the Knowledge Related Articles widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of related articles mapped to an article.

## Before you begin

Role required: sp\_admin or admin

## About this task

The knowledge article view page displays the Related Articles section when an article has related articles. Use the widget instance options to customize the Related Articles section on the article view page.

## Procedure

1.  Navigate to the Knowledge Management homepage in the Knowledge Management Service Portal by adding `/kb` to the end of the URL for your instance.

    **Note:** You can change the default navigation by configuring the property **sn\_km\_portal.glide.knowman.serviceportal.portal\_url**.

2.  Click to open the article for which you want to modify the instance options for the Knowledge Related Articles widget.

3.  On the article page, press Control+right-click and select **Page in Designer**.

4.  In the Service Portal Designer page, click the edit icon \(![edit](../image/Edit.png)\) on **Knowledge Related Articles** widget to add the related articles.

    **Note:** You can also add **Knowledge Related Articles** widget using **Widgets** search field and drag-and-drop the widget to the blank field.

5.  Configure settings for the Knowledge Related Articles widget.

    |Instance option|Description|
    |---------------|-----------|
    |Title|Title that appears on the widget header. The default title is Related Articles.|
    |Bootstrap color|Color scheme of the widget header. Select a color for your widget from a list of common bootstrap colors.|
    |Glyph|Icon that appears beside each list item displayed in the widget. To skip this field, select the empty glyph.|
    |CSS|Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/scss-primer.md).|
    |Use Full Width|Option for displaying the widget in a 12-column grid at 100% of the available width. If you clear the check box, the widget displays at 75% of the available width.|
    |Table|The table that contains the knowledge articles associated with the **Display Fields** and **Secondary Fields**. By default, the table is Knowledge \(kb\_knowledge\).|
    |Display Field|The title displayed for each article in the related articles list. The display field specified in the base system is the article short description.|
    |Secondary Fields|Additional information displayed for each article in the list below the title. The secondary fields specified in the base system are author, view count, the last modified date of the article, and the article rating.|
    |Max number of records to show|The maximum number of articles to include in the Related Articles section on the article view page. The maximum number specified in the base system is 5.|
    |Show even when empty|Option for displaying the widget even if no articles are in the list.|
    |Show Secondary Fields Label|Options for displaying the field labels for the additional information displayed for each article.|
    |Knowledge Base|To restrict the articles that appear in this list to a specific knowledge base, select the knowledge base from the knowledge base list.|
    |Source Table|Source table containing related articles. The source table specified in the base system is Knowledge \(kb\_2\_kb\).|
    |Source Column|Field in the source table referring to the source record. The source column specified in the base system is Knowledge article \(kb\_knowledge\).|
    |Target Column|Field in the source table referring to the target record. The target column specified in the base system is Knowledge article \(kb\_knowledge\).|
    |Source Id|URL parameter containing the unique record identifier \(sys\_id\) of the source record. For the article view page, the URL parameter containing the source ID is sys\_kb\_id.|

6.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

**Related topics**  


[Map related articles](map-related-articles.md)

[Knowledge Management Service Portal properties](../reference/knowledge-service-portal-properties.md)

