---
title: Display ServiceNow knowledge articles on an Adobe Experience Manager page
description: Use knowledge components available within Adobe Experience Manager \(AEM\) to access knowledge bases from the ServiceNow instance and display associated knowledge articles on an AEM-based website.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Integrating with Adobe Experience Manager, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Display ServiceNow knowledge articles on an Adobe Experience Manager page

Use knowledge components available within Adobe Experience Manager \(AEM\) to access knowledge bases from the ServiceNow instance and display associated knowledge articles on an AEM-based website.

## Before you begin

-   Activate the Knowledge API plugin \(sn\_km\_api\) to use the Knowledge Management REST API endpoints for knowledge articles. For more information, see [Knowledge Management REST API](https://www.servicenow.com/docs/access?context=knowledge-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   Define the cross-origin resource sharing \(CORS\) rule to access the Knowledge API from your AEM instance. For more information, see [Define a cross-origin resource sharing rule to access ServiceNow API endpoints from AEM](aem-set-cors-rules-1.md).

Role required: AEM author

## Procedure

1.  Log in to your AEM instance.

2.  Open your AEM page in [Edit mode](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/author-environment-tools.html#main-pars_title_20).

3.  Open the [components browser](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/author-environment-tools.html#main-pars_title_17).

4.  From the **All** list, select **ServiceNow**.

5.  Drag a component to the required position on the page.

    **Note:** If components are not available, update your template configuration to include the knowledge components. In addition, you must modify the properties of the site template and add each knowledge article component to the list of allowed components.

6.  Open the [component dialog for editing](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/editing-content.html#ComponentEditDialog).

    **Note:** By default, the knowledge components in the Edit mode of a page in AEM aren't accessible by public users, which are anonymous AEM users who are not logged in. To change the default behavior, you must enable the **Public** property for each knowledge component.

7.  Set the Search Results component properties to display knowledge search results that include a list of knowledge articles from the knowledge bases in the ServiceNow instance.

<table id="table_kx2_4q2_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td id="component-public">

Public

</td><td id="component-public-desc">

Option to make the content of the component visible to public users. When selected, the knowledge articles available to unauthenticated users included in the component are available to all users, including public users.

</td></tr><tr><td id="component-kb">

Knowledge Bases

</td><td id="component-kb-desc">

System identifier \(sys\_id\) of a knowledge base that contains associated knowledge articles. Click **Add field** and enter the sys\_id of a knowledge base. You can add multiple entries.

 **Note:** If you don't add a value, knowledge bases from the OSGi configuration settings are used for ServiceNow components.

</td></tr><tr><td id="component-lan">

Language

</td><td id="component-lan-desc">

Enables the display of knowledge article search results in different languages. Select one of the following options:

-   **Select from ServiceNow OSGi Configuration**: Knowledge articles are displayed in the language configured in the OSGi configuration for ServiceNow components. This value is selected by default.
-   **Restrict to portal language**: Knowledge articles are displayed in the language configured in the AEM site.
-   **All languages**: Knowledge articles are displayed in all languages.


</td></tr><tr><td id="component-search">

Search parameter

</td><td id="component-search-desc">

Parameter key for the search query. Example: `kb_query`

</td></tr><tr><td id="component-secondary">

Secondary fields

</td><td id="component-secondary-desc">

Metadata of a knowledge article that appear with the article. Metadata include information such as the author, the date the article was last updated, and the date the article was last viewed. For multiple entries, separate the fields by commas. Example: `author,sys_view_count,sys_updated_on,rating`

</td></tr><tr><td>

Search results count

</td><td>

Maximum number of articles included in the search results list.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td id="component-article-page">

Article page URL

</td><td id="component-article-page-desc">

Relative URL of the article page to redirect to. Example: `/content/NOWApp/now_article_view.html`

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [../concept/aem-style-components-1.md\#](../concept/aem-style-components-1.md#).

</td></tr></tbody>
</table>8.  Set the Search Box component properties to display a search box for users to enter search text and find knowledge articles in the ServiceNow instance matching the search text.

    **Note:** Triggering a search from the Search Box component leads to the Search Results component.

<table id="table_cbh_dlp_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Public

</td><td>

Option to make the content of the component visible to public users. When selected, the knowledge articles available to unauthenticated users included in the component are available to all users, including public users.

</td></tr><tr><td>

Placeholder

</td><td>

Hint text displayed in the search box to provide information about what users can search for or conditions for the search text. Example: `Search (minimum three characters)`

</td></tr><tr><td>

Knowledge Bases

</td><td>

System identifier \(sys\_id\) of a knowledge base that contains associated knowledge articles. Click **Add field** and enter the sys\_id of a knowledge base. You can add multiple entries.

 **Note:** If you don't add a value, knowledge bases from the OSGi configuration settings are used for ServiceNow components.

</td></tr><tr><td>

Language

</td><td>

Enables the display of knowledge articles in different languages in the search box. Select one of the following options:

-   **Select from ServiceNow OSGi Configuration**: Knowledge articles are displayed in the language configured in the OSGi configuration for ServiceNow components. This value is selected by default.
-   **Restrict to portal language**: Knowledge articles are displayed in the language configured in the AEM site.
-   **All languages**: Knowledge articles are displayed in all languages.


</td></tr><tr><td>

Search page URL

</td><td>

Relative URL of the search page to redirect to. Example: `/content/NOWApp/now_article_search.html`

</td></tr><tr><td>

Search parameter

</td><td>

Parameter key for the search query. Example: `kb_query`

</td></tr><tr><td>

Typeahead

</td><td>

Option to enable typeahead search.

</td></tr><tr><td>

Typeahead search results count

</td><td>

Maximum number of articles to include in the typeahead search results list.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td>

Article page URL

</td><td>

Relative URL of the article page to redirect to. Example: `/content/NOWApp/now_article_view.html`

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [../concept/aem-style-components-1.md\#](../concept/aem-style-components-1.md#).

</td></tr></tbody>
</table>9.  Set the Article View component properties to display knowledge articles and their attachments, if available, from a ServiceNow instance.

<table id="table_tfp_h4q_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Public

</td><td>

Option to make the content of the component visible to public users. When selected, the knowledge articles available to unauthenticated users included in the component are available to all users, including public users.

</td></tr><tr><td>

Article parameter

</td><td>

Name of the URL query parameter for the article number. Example: `kb_article`

</td></tr><tr><td>

Secondary fields

</td><td>

Metadata of a knowledge article that appear with the article. Metadata include information such as the author, the date the article was last updated, and the date the article was last viewed. For multiple entries, separate the fields by commas. Example: `author,sys_view_count,sys_updated_on,rating`

</td></tr><tr><td>

Language parameter

</td><td>

Name of the URL query parameter containing the requested language for a knowledge article. Example: `kb_lang`

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [../concept/aem-style-components-1.md\#](../concept/aem-style-components-1.md#).

</td></tr></tbody>
</table>10. Set the Article List component properties to display a list of knowledge articles depending on the list criteria.

<table id="table_ywq_wbr_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Public

</td><td>

Option to make the content of the component visible to public users. When selected, the knowledge articles available to unauthenticated users included in the component are available to all users, including public users.

</td></tr><tr><td>

Title

</td><td>

Title corresponding to the articles list that appears as the component header. Example: `Most viewed articles`

</td></tr><tr><td>

Knowledge Bases

</td><td>

System identifier \(sys\_id\) of a knowledge base that contains associated knowledge articles. Click **Add field** and enter the sys\_id of a knowledge base. You can add multiple entries.

 **Note:** If you don't add a value, knowledge bases from the OSGi configuration settings are used for ServiceNow components.

</td></tr><tr><td>

Language

</td><td>

Enables the display of a knowledge article in different languages when viewing the article. Select one of the following options:

-   **Select from ServiceNow OSGi Configuration**: Knowledge articles are displayed in the language configured in the OSGi configuration for ServiceNow components. This value is selected by default.
-   **Restrict to portal language**: Knowledge articles are displayed in the language configured in the AEM site.
-   **All languages**: Knowledge articles are displayed in all languages.


</td></tr><tr><td>

Secondary fields

</td><td>

Metadata of a knowledge article that appear with the article. Metadata include information such as the author, the date the article was last updated, and the date the article was last viewed. For multiple entries, separate the fields by commas. Example: `author,sys_view_count,sys_updated_on,rating`

</td></tr><tr><td>

Criteria

</td><td>

List of criteria for the knowledge articles list. Select one of the following options:-   **Featured**: List of featured knowledge articles based on the keywords configured in the **glide.knowman.default\_keyword** property. For information about featured articles, see [Add a knowledge article to featured content](https://www.servicenow.com/docs/access?context=t_PinAnArticle&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Knowledge properties](https://www.servicenow.com/docs/access?context=r_KnowledgeProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   **Most Viewed**: List of knowledge articles with the most views.


</td></tr><tr><td>

Article count

</td><td>

Maximum number of articles to include in the articles list. Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td>

Article page URL

</td><td>

Relative URL of the article page to redirect to. Example: `/content/NOWApp/now_article_view.html`

</td></tr><tr><td>

Hide component when empty

</td><td>

Option to hide the component when there are no knowledge articles to display.

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [../concept/aem-style-components-1.md\#](../concept/aem-style-components-1.md#).

</td></tr></tbody>
</table>
