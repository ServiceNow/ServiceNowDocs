---
title: Integrating Knowledge Management features with the Service Portal
description: To create a consistent user experience for Knowledge Management, integrate Knowledge Management Service Portal in your end-user facing Service Portal.Use a page route map to access the enhanced Knowledge Management homepage from the Service Portal homepage.Use a custom knowledge search widget to access the enhanced Knowledge Management search results page from the Service Portal search results page.Add the Knowledge Management Service Portal widgets Featured Articles, Most Useful Articles, and Most Rated Articles to the Service Portal homepage to quickly access knowledge articles.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrating Knowledge Management features with the Service Portal

To create a consistent user experience for Knowledge Management, integrate Knowledge Management Service Portal in your end-user facing Service Portal.

The Knowledge Management Service Portal includes the following features:

-   Multiple knowledge bases
-   A Knowledge Management article view page with feedback options
-   A Knowledge Management search results page with options to filter and sort search results
-   A number of widgets to enable searches, display search results, display knowledge articles, and so on

By default, all knowledge articles in the Service Portal are redirected to the Knowledge Management article view page using the **Knowledge Article View** page route map. If upgrading from a previous release, a system administrator can activate the **Knowledge Article View** page route map to take advantage of the features of the Knowledge Management article view page. For more information, see [Activate the Knowledge Article View page on upgrade](https://www.servicenow.com/docs/access?context=redirect-knowledge&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

**Note:** The Knowledge Management Service Portal supports only Zing search and not AI search.

System administrators perform the following tasks to integrate the Knowledge Management Service Portal features with the Service Portal:

-   [Integrate the Knowledge Management homepage with the Service Portal homepage](conf-service-portal-know-management.md#).
-   [Integrate the Knowledge Management search results page with the Service Portal search results page](conf-service-portal-know-management.md#).
-   [Add the Knowledge Management Service Portal widgets to quickly access knowledge articles from the Service Portal homepage](conf-service-portal-know-management.md#) \(Optional\).

**Note:** These configurations apply to the base system pages within the Service Portal only.

**Parent Topic:**[Configure the Knowledge Management Service Portal](knowledge-management-service-portal.md)

**Related topics**  


[Service Portal pages](https://www.servicenow.com/docs/access?context=c_Pages&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

[Knowledge Management Service Portal homepage features](knowledge-service-portal-pages.md)

[Using search in Knowledge Management Service Portal](knowledge-service-portal-search.md)

[Knowledge Management Service Portal article view page features](knowledge-service-portal-view.md)

## Integrate the Knowledge Management homepage with the Service Portal homepage

Use a page route map to access the enhanced Knowledge Management homepage from the Service Portal homepage.

### Before you begin

The Knowledge Management - Service Portal plugin \(com.snc.knowledge\_serviceportal\) is activated.

**Note:** This plugin is activated by default for customers on Madrid and later releases. Existing customers on release versions prior to Madrid must activate the plugin to perform this configuration task. For more information, see [Activate the Knowledge Management Service Portal plugin](../task/activate-km-service-portal-plugin.md).

Role required: admin

### About this task

The Knowledge Management homepage displays knowledge articles organized by knowledge base and category, featured content, and popular articles. You use a page route map to access the Knowledge Management homepage from the Service Portal homepage.

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Click **New**.

3.  On the Page Route Map form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Service Portal\(s\)|Service Portal|
    |Route from|kb\_view2|
    |Route to|kb\_home|
    |Active|Selected|

    **Note:** On the Page Route Map form, you can fill in the **Short Description** and **Order** fields as appropriate.

4.  Click **Submit**.


### Result

You can now open the Knowledge Management homepage from the Service Portal homepage by clicking the Knowledge link or Knowledge Base icon link.

## Integrate the Knowledge Management search results page with the Service Portal search results page

Use a custom knowledge search widget to access the enhanced Knowledge Management search results page from the Service Portal search results page.

### Before you begin

Role required: admin

### About this task

The Knowledge Management search results page in the Knowledge Management Service Portal includes options to filter and sort search results and a number of widgets to enable searches, display search results, display articles, and so on. In this procedure, to access the Knowledge Management search results page from the Service Portal search results page, you create a custom knowledge search widget named Search Within and add it to the Service Portal search results page.

### Procedure

1.  Create a custom knowledge search widget named Search Within.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  On the Service Portal page, click **Widget Editor**.

    3.  Click **Create a new widget**.

    4.  In the Add a Widget dialog box, in the **Widget Name** field, enter `Search Within`.

        The **Widget ID** field is automatically populated based on the widget name.

    5.  Click **Submit**.

        The widget HTML template, client script, and server script display in the widget editor.

    6.  In the widget editor, enter the following field values to replace any existing text.

        -   In the **HTML Template** field, enter the following code to add a link to the Knowledge Management search results page in the Search Within widget from the Service Portal.

            ```
            <div role="list" class="list-group">
              <span class="list-group-item active">${Search Within}</span>
              <a role="link" class="list-group-item" ng-href="{{data.url}}">${Knowledge}</a>
            </div>
            ```

        -   In the **Server Script** field, enter the following code to set the URL parameters for the Knowledge Management search results page:

            ```
            (function(){
            	var q = encodeURIComponent($sp.getParameter('q'));
            	var kb = $sp.getValue('kb_knowledge_base') || "";
            	data.url = '/sp?id=kb_search';
            	if(q)
            		data.url += "&keyword="+q;
            	if(kb)
            		data.url += "&kb_knowledge_base="+kb;
            })();
            ```

        **Note:** For more information about these fields, see [Widget developer guide](https://www.servicenow.com/docs/access?context=widget-dev-guide&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    7.  Click **Save**.

2.  Add the custom knowledge search widget to the Service Portal search results page.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  Click **Designer**.

    3.  In the **Filter by title or Id** field, enter `sp_search`, the ID for the Service Portal search results page, and then select **Search**.

    4.  In the **Filter Widget** field, search for the Search Within widget and drag it onto the container where you want the widget to appear on the Service Portal search results page.![Search Within widget](../image/search-within-widget.png)

        **Tip:** To verify the location and appearance of the newly added Search Within widget on the Service Portal search results page, click the **Preview** tab.

    The Search Within knowledge search widget is added to the Service Portal search results page. Clicking **Knowledge** in the widget and searching for a keyword will redirect you to the Knowledge Management search results page in the Knowledge Management Service Portal.


## Add widgets to access knowledge articles from the Service Portal homepage

Add the Knowledge Management Service Portal widgets Featured Articles, Most Useful Articles, and Most Rated Articles to the Service Portal homepage to quickly access knowledge articles.

### Before you begin

Role required: admin

### About this task

For more information about Knowledge Management Service Portal widgets, see [Knowledge Management Service Portal widgets](km-service-portal-widget-instances.md).

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Click **Designer**.

3.  Select the Service Portal homepage.

4.  In the **Filter by title or Id** field, enter `index`, the ID for the Service Portal homepage, and then select **Service Portal**.

5.  In the **Filter Widget** field, search for the following Knowledge Management Service Portal widgets, and then drag them onto the container where you want them to appear on the Service Portal homepage.

    |Widget Name|Widget Display Name|
    |-----------|-------------------|
    |**Knowledge Featured Articles**|Featured Articles|
    |**Knowledge MostUseful Articles**|Most Useful Articles|
    |**Knowledge MostViewed Articles**|Most Viewed Articles|

    **Tip:** To verify the location and appearance of the added widgets on the Service Portal, click the **Preview** tab.


### Result

Clicking a knowledge article link from one of the added widgets on the Service Portal homepage opens the Knowledge Management article view page in the Knowledge Management Service Portal.

