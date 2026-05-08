---
title: KB Category Page widget
description: Articles and article preview within a particular category. Categories are specified within the Knowledge Base module. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Knowledge Management widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# KB Category Page widget

Articles and article preview within a particular category. Categories are specified within the Knowledge Base module. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The KB Category Page widget works together with the [KB Categories widget](kb-categories-widget.md). When you select a category in the KB Categories widget, the KB Category page widget lists articles within that category.

To have the KB Categories and KB Category Page widgets work in tandem, add the two widgets to the same page.

If you add the KB Category Page widget to a page without adding the KB Categories widget, the KB Category Page widget displays an uncategorized list of all articles within the knowledge base.

Categories are determined by the list of Knowledge Categories provided for the Knowledge Base. To view a list of categories for a knowledge base, in the platform navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge bases**, then select the name of the knowledge base, for example IT. Categories for the knowledge base appear in the related lists. If a category does not have any associated articles, it does not appear in the portal. For more information on defining categories for a knowledge base, see Define a knowledge article category.

The knowledge base that a portal uses is determined in the portal form. For more information on associating your portal with a knowledge base, see [Associate a portal with a knowledge base](../task/associate-portal-knowledge.md).

## Instance options

![KB category widget with instance options for bootstrap color and star rating](../image/IOKBCategoryPage.png "KB category widget instance options")

|Field|Description|
|-----|-----------|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Show star rating|Displays the star rating on the category page. If you select **Use system properties**, the appearance of the star rating is defined by the **glide.knowman.show\_star\_rating** system property.|

**Parent Topic:**[Knowledge Management widgets](km-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

