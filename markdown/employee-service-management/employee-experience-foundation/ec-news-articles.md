---
title: News articles
description: The News article content type combines content creation features from the Rich Content Editor with new publishing methods that enable high volume content publishing to the portal and Now Mobile app to keep employees updated on company news and announcements.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Creating employee communications, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# News articles

The News article content type combines content creation features from the Rich Content Editor with new publishing methods that enable high volume content publishing to the portal and Now Mobile app to keep employees updated on company news and announcements.

## News articles in the employee portal

News articles are delivered to users through customizable instances of the News Feed widget. The News Feed widget instances appear on the portal Home page, News Center, Article detail page, and the emp\_taxonomy\_topic page. The admin can configure the News Feed widget to display news articles in a vertical list or as a three-column grid, add a call to action that links to another page, or to display the news categories. For more information, see [Modify the News feed widget](../task/modify-news-feed-widget-display.md).

The Featured News widget appears at the top of the News Center page to display highlighted news articles. For information on configuring the Featured News widget, see [Modify the Featured News widget](../task/modify-featured-news-widget.md).

For ServiceNow instances that are on version Washington or later, the News Center automatically appears as a menu option in the top-level navigation menu \(mega menu\) to give users quick access to all the published news articles. To remove it from the menu, see [Hide News Center from the Mega Menu](../task/hide-news-center-mega-menu.md).

Review the following graphic to understand how employees see and interact with the widgets that display News articles:![The News Center contains the Featured news widget, with the News feed widget underneath. News articles open in a new page with the Other news widget on the side.](../images/ec-news-center-page.png)

1.  News Center widget displays highlighted articles on the home page
2.  News Center button opens the News Center page
3.  Featured News widget displays highlighted articles in the News Center page.
4.  All news list uses the News feed widget to show news configured for delivery to this page
5.  When an employee clicks a news article, the full article opens in the Article details page

    The three subsequent widgets \(News info, News Header, and News Article Detail\) work in tandem to display a news article. The three widgets contain the instance option **Use dataloader**. We recommend enabling this option as it allows the news widgets to share data with each other, which reduces calls to the server and web page loading time.

6.  News Info widget: Holds the Published date and Copy Link button
7.  News Header widget: Holds the headline, subheadline and image thumbnail
8.  News Article Detail widget: Holds the article body as created in the Rich Content
9.  Other news uses the News feed widget to show news configured for delivery to this page

## Searching for news articles

When employees enter a keyword in the global search bar, Employee Center uses AI Search to return published news articles containing that keyword in the heading, subheading, article content, or category.

![Searching for by keyword "employee" returns a news article with the term in the article content](../images/ec-news-search.png)

AI Search returns additional results based on user roles:

-   Users with either the system admin or content admin role can see unpublished content.
-   For users with the content manager, content admin, or content approver roles, search results include content for which they are not the audience. However, they cannot view the content unless they are part of the configured audience.

## Employee engagement with news articles

Content engagement enhances news articles by providing users with a way to comment and react to articles and for managers to measure the effectiveness of their content using engagement metrics. For more information, see [Content engagement](ec-content-engagement.md)

![Content engagement delivers engagement summary, reaction icons, and commenting capabilities to the portal](../images/emp-engagement.png)

## News articles in the Now Mobile app

The Now Mobile app features the News center screen, which displays the same News articles that are published to the News feed widget in the portal. In addition, content managers can configure News articles to appear on the Now Mobile app Home screen.

![Now Mobile app home page has a section for Featured news and the News Center screen](../images/ec-news-mobile.png)

For information on the Now Mobile app user experience, see [News in Now Mobile](news-ec-mobile.md). For information on publishing news articles, see [Create a publish plan for your content](../task/ec-content-library-publish2.md).

## Organizing news articles

Content admins and managers can assign one or more categories to a news article, for example Industry news or Company culture. Once the article is published, employees can see the categories associated with an article when previewing it in the News Feed widget on the Home page or in the News Center. An employee can click the category to open the Category page, which lists all the news articles associated to that category in reverse chronological order.

The following table demonstrates how categories enhance the user experience:

<table id="table_mnk_ckf_gzb"><thead><tr><th>

Capability

</th><th>

Screen shot

</th></tr></thead><tbody><tr><td>

When an employee searches for a news article, they can filter the search results by news category.

</td><td>

![Employees can filter search results by news category](../images/ec-news-categories-search.png)

</td></tr><tr><td>

The News Feed widget displays the categories for each article, which link to a page for that category. Each category page lists the associated news articles, organized by publication date, with the most recently published articles displayed first.

The page also holds a Category list widget with links to the other category pages. The widget displays the categories based on the configured order. If there are multiple categories with the same order value, the system lists them in alphabetical order.

</td><td>

![News articles in the News feed widget display their category. When clicked, the link redirects to a page that lists all the news articles for that category](../images/ec-news-category.png)

</td></tr><tr><td>

The News Center holds a Category list widget with links to the category pages. When an employee opens a news article, the Article detail page displays the news category at the bottom of the article.

</td><td>

![News articles display their associated category](../images/ec-news-category-article.png)

</td></tr></tbody>
</table>## Boosting News article production

Content authors can increase their productivity by leveraging content templates to produce large volumes of News articles. A user with the sn\_cd.content\_template\_owner role first creates a content template to define the article layout, publishing location, and audience. When a content author creates a new article, they can associate the news article to a content template to access a pre-built template and auto-generated publish plans.

For more information, see [Content templates](ec-content-templates.md).

## Customizing the News experience

The News Center and Article Detail pages support other Content Publishing widgets. For example, you can configure the News Center page to display upcoming events. For information on configuring the portal pages, see [Creating portal pages](https://www.servicenow.com/docs/access?context=c_Pages&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

To set a limit for the number of articles displayed in the News widget or to select different pages for the News Center or Article display, see the News section of [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

If you plan to customize the News Center or Article details page, we recommend that you create new pages and update the properties to redirect to the new pages. Some additional considerations include:

-   The Article details page widgets require a `sys_id` query string parameter with the sys\_id of the specific News Article.
-   We recommend having a News Dataloader widget in the Article details page, and enabling the **Use Dataloader** option in the other widgets in the page. This facilitates data sharing between the widgets on the page, which reduce the page loading time.

