---
title: KB Categories widget
description: Lists the categories for your Knowledge Base. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# KB Categories widget

Lists the categories for your Knowledge Base. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Knowledge Base categories widget](../image/WidgetKBCategories.png "KB Categories widget")

Categories are determined by the list of Knowledge Categories provided for the Knowledge Base. To view a list of categories for a knowledge base, in the platform navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge bases** then select the name of the knowledge base, for example IT. Categories for the knowledge base appear in the related lists. For more information on defining categories for a knowledge base, see [Define a knowledge article category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/t_DefineAKnowledgeCategory.md).

**Note:** If the **Max article limit to allow category counts** field is set to 500 counts and the knowledge base contains more than 500 articles the KB categories widget displays all of the categories in the knowledge base.

The knowledge base that a portal uses is determined in the portal form. If your portal uses multiple knowledge bases, you can use the [KB Knowledge Bases widget](knowledge-bases-widget.md) to filter the content of the KB Categories widget.

For more information on associating your portal with a knowledge base, see [Associate a portal with a knowledge base](../task/associate-portal-knowledge.md).

**Note:** In the widget Instance Options, if the **Max number of articles evaluated per category to determine visibility** value is set to 1 or higher the user must have access to at least one article in the category for the category to be displayed.

## Instance options

The KB categories widget does not include instance options.

**Parent Topic:**[Knowledge Management widgets](km-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

