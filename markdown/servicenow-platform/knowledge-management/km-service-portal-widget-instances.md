---
title: Knowledge Management Service Portal widgets
description: The Knowledge Management Service Portal uses a number of widgets to enable searches, display search results, and display articles, related articles, and related items.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management Service Portal widgets

The Knowledge Management Service Portal uses a number of widgets to enable searches, display search results, and display articles, related articles, and related items.

In the Knowledge Management Service Portal, the Knowledge Management homepage, search results page, and article view page honor the Knowledge Management V3 system properties. If configured, widget instance options can override the system properties.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](knowledge-service-portal-pages.md).

Users with the knowledge\_admin or admin role can configure the widget instance options used on the Knowledge Management Service Portal pages. Use the control + right-click menu to access the widget instance options and configure a widget instance. For more information, see [Configure widget instance options](https://www.servicenow.com/docs/access?context=c_ConfigureWidgetInstances&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

**Note:** Before configuring widget instance options, switch to the Knowledge Management - Service Portal scope.

Homepage widgets:

-   [Knowledge Homepage Search](../task/config-search-widget-options.md)

    Customize search features for the homepage.

-   [Knowledge Bases Browse](../task/config-kb-tile-widget-options.md)

    Displays knowledge base tiles in the homepage.

-   [Knowledge Featured Articles](../task/config-homepage-widget-options.md)

    Displays a list of featured articles in the homepage.

-   [Knowledge Most Useful Articles](../task/config-homepage-widget-options.md)

    Displays a list of most useful articles in the homepage.

-   [Knowledge Most Viewed Articles](../task/config-homepage-widget-options.md)

    Displays a list of most viewed articles in the homepage.


Search results page widgets:

-   [Knowledge Breadcrumbs](https://www.servicenow.com/docs/access?context=knowledge-breadcrumbs&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

    Displays navigation path to the current page and a search box for users to search the knowledge base.

-   [Knowledge Search](../task/config-search-widget-options.md)
-   Knowledge Facet Header

    Displays the title for the filter facets.

-   [Knowledge Field Facet](../task/config-search-results-filter-facets.md)

    Display search results filtered by knowledge base, knowledge category, and author.

-   [Knowledge Tags Facet](../task/config-search-results-filter-facets.md)

    Display search results filtered by article tags.

-   [Knowledge Resource Facet](../task/config-search-results-filter-facets.md)

    Display search results filtered by article resource.

-   [Knowledge Query Facet](../task/config-search-results-filter-facets.md)

    Display search results filtered by article rating, number of article views, and last modified.

-   [Knowledge Result Sort](../task/config-search-results-sort-options.md)

    Displays search results filtered by sort options for returned results.

-   Knowledge Selected Filter

    Displays the selected facet filters and allows you to clear the selections.

-   [Knowledge Result](../task/config-search-results-list-options.md)

    Displays search results filtered by returned results.


Article view page widgets:

-   Knowledge Breadcrumbs

    Displays navigation path to the current page.

-   [Knowledge Article Content](../task/config-user-action-on-article-view.md)

    Customize what information users can view and what actions they can perform in the article view page.

-   [Knowledge Article Helpful](../task/config-knowledge-article-helpful.md)

    Enables users to mark the article as helpful.

-   [Knowledge Article Comments](../task/config-knowledge-article-comments.md)

    Enables users to add comments for the article.

-   Knowledge Attachments

    Displays article attachments if the **Display Attachment** field for the article is enabled.

    **Note:** You must add the Knowledge Attachments widget to any page in addition to Knowledge Article Content widget. After upgrade, if this widget does not get added automatically, you must add it manually.

-   [Related Catalog Item](../task/configure-related-items-widget.md)

    Displays a list of catalog items mapped to the article. The widget appears only when the related catalog items are available for the selected article.

-   [Knowledge Related Articles](../task/configure-related-articles-widget.md)

    Displays a list of related articles with information similar to the selected article. The related articles are manually mapped, automatically predicted, or both. The manually mapped articles appear first in the widget. The widget appears only when the related articles are available for the selected article.

-   Affected Products

    Displays the products related to the knowledge articles available in the **Affected Products** related list for the article. The widget appears only when the affected products are available for the selected article.

-   Most Recent Tasks

    Displays the tasks attached to the articles available in the **Attached Tasks** related list for that article. The widget appears only when the related tasks are available for the selected article.

-   [Most Useful](../task/config-homepage-widget-options.md)

    Displays a list of knowledge articles that users found most useful.


-   **[Activate the Knowledge Management Service Portal plugin](../task/activate-km-service-portal-plugin.md)**  
The Knowledge Management - Service Portal plugin \(com.snc.knowledge\_serviceportal\) is active by default for customers on Madrid and later releases. Existing customers on release versions prior to Madrid can activate the plugin, if required.
-   **[Configure search widget instance options](../task/config-search-widget-options.md)**  
Configure widget instance options for the search widgets on the Knowledge Management Service Portal homepage and search results page.
-   **[Configure knowledge base tile widget instance options](../task/config-kb-tile-widget-options.md)**  
Configure widget instance options for the knowledge base tile widgets on the Knowledge Management Service Portal homepage.
-   **[Configure the home page widget instance options](../task/config-homepage-widget-options.md)**  
Configure widget instance options for the widgets used to display popular articles on the Knowledge Management Service Portal homepage.
-   **[Configure sort widget instance options](../task/config-search-results-sort-options.md)**  
Configure widget instance options for the knowledge sort widget on the Knowledge Management Service Portal search results page.
-   **[Configure article list widget instance options](../task/config-article-list-widget-options.md)**  
Configure widget instance options for the article lists on the Knowledge Management Service Portal homepage.
-   **[Configure search results list widget instance options](../task/config-search-results-list-options.md)**  
Configure widget instance options for the results list widget on the Knowledge Management Service Portal search results page.
-   **[Configure filter facet widget instance options](../task/config-search-results-filter-facets.md)**  
Configure widget instance options for the filter facet widgets on the Knowledge Management Service Portal search results page.
-   **[Configure a user action for the article view page](../task/config-user-action-on-article-view.md)**  
Configure a user action for the Knowledge Management article view page in the Knowledge Management Service Portal.
-   **[Configure article helpful widget instance options](../task/config-knowledge-article-helpful.md)**  
Configure the Knowledge Article Helpful widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.
-   **[Configure article comments instance options](../task/config-knowledge-article-comments.md)**  
Configure the Knowledge Article Comments widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal.
-   **[Configure related catalog item widget instance options](../task/configure-related-items-widget.md)**  
Configure the Related Catalog Item widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of catalog items mapped to an article.
-   **[Configure knowledge related articles widget instance options](../task/configure-related-articles-widget.md)**  
Configure the Knowledge Related Articles widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of related articles mapped to an article.

**Parent Topic:**[Configure the Knowledge Management Service Portal](knowledge-management-service-portal.md)

