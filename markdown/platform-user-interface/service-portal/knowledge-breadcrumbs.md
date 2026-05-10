---
title: Knowledge Breadcrumbs widget
description: Help users navigate a knowledge base by adding the Knowledge Breadcrumbs widget. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Knowledge Management widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Knowledge Breadcrumbs widget

Help users navigate a knowledge base by adding the Knowledge Breadcrumbs widget. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

The knowledge breadcrumbs widget displays information based on where an article is located in a knowledge base. For example, if you open an article on "How to Deal with Spam," the breadcrumbs show that the article is located in the Email category of the IT knowledge base.

![The Knowledge Breadcrumb widget](../image/knowledge-breadcrumb.png)

You can broaden your search of the knowledge case by selecting the titles in the breadcrumbs. For example, to see all articles in the Email category, you would select **Email**. To see all articles in the knowledge base, you would select **IT \(Knowledge Base\)**.

The widget also includes a search box so that you can search for an article by name.

## Instance options

Use the instance options to configure the Knowledge Breadcrumbs widget for a portal page.

**Note:** The AI Search instance options apply only if AI Search is enabled in your portal. For more information on enabling AI Search for Service Portal, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

<table id="table_jtv_wws_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Show Search Box

</td><td>

Option to include a search box for users to search the knowledge base.

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Search Application

</td><td>

Defines search experience settings for the widget, such as the search engine, search results limit, and suggestions limit. By default, the widget uses the same search application configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search application configuration, see [Defining search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-app-cfgs-ais.md).

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed after using the widget. By default, the widget uses the same search results configuration as the portal, but you can override this configuration at the widget level.

 For more information on defining a search results configuration, see [Define a composite dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/define-composite-dataset.md).

</td></tr><tr><td>

Disable All Suggestions

</td><td>

Option to disable search suggestions.

</td></tr><tr><td>

Placeholder

</td><td>

Text that appears in the search box before the user enters anything.

</td></tr><tr><td>

AI Search Source Filter

</td><td>

Content that portal users can search on, including tables in your instance or external data sources. For more information, see [Defining search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).

</td></tr></tbody>
</table>**Parent Topic:**[Knowledge Management widgets](km-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

