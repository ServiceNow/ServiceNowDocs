---
title: Knowledge Management properties
description: As an administrator, you can configure the look and functionality of many knowledge base features with Knowledge Management properties.Knowledge portal properties control the look and functionality of the legacy portal page. This portal page lists recent knowledge articles and their publishing dates, organized by topic.Knowledge search properties give you control over the search options available to users and the presentation of search results.Article view properties give you control over the meta data and rating options that appear with articles. They also enable you to grant access to individual feedback options based on user role.Knowledge homepage properties control the featured content on the knowledge homepage.Other knowledge properties let you control general knowledge management features.The knowledge administrator can set knowledge properties that enable users to edit specific fields on published articles without creating new versions.The knowledge administrator can set configuration properties that enable users to subscribe to knowledge bases and knowledge articles.The knowledge administrator can set the pass score for AQI reviews using the knowledge properties page.Administrators can configure the properties to add allowed content types and change the UI label for the external content integration feature.The Knowledge administrator can set configuration properties that would create actionable feedback tasks.The knowledge administrator can set group ownership properties that enable the use of ownership groups for knowledge articles and decide who can edit and approve a published knowledge article.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 32
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management properties

As an administrator, you can configure the look and functionality of many knowledge base features with Knowledge Management properties.

You can access Knowledge Management properties by navigating to **Knowledge** &gt; **Administration** &gt; **Properties**.

**Parent Topic:**[Knowledge Management reference](knowledge-management-reference.md)

## Knowledge portal properties

Knowledge portal properties control the look and functionality of the legacy portal page. This portal page lists recent knowledge articles and their publishing dates, organized by topic.

<table id="table_mnk_g4c_54"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of columns on Knowledge portal pages \(**glide.knowman.columns**\)

</td><td>

Set the number of columns for arranging topics on the knowledge portal.**Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Maximum number of articles per content block on the home page \(**glide.knowman.content\_block\_limit**\)

</td><td>

Enter the maximum number of articles to display in the Most Useful and Most Viewed sections of the knowledge homepage.**Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Omit empty Knowledge topics and categories \(**glide.knowman.show\_only\_populated**\)

</td><td>

Select the check box to display topic sections only if there are articles for the topic. Clear the check box to show all topic sections, even those with no assigned articles.**Note:** This property does not apply to the New category.

This property applies only to the default knowledge base and the legacy knowledge portal. Knowledge Management v3 articles do not specify a topic. Therefore, this property applies only to Knowledge v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Show Knowledge section descriptions \(**glide.knowman.show\_descriptions**\)

</td><td>

Select the check box to display topic descriptions in the knowledge portal. To enter these descriptions:1.  Edit an existing knowledge article.
2.  Right-click the Topic field label and choose Show Choice List.
3.  Open the record for the topic name and enter the description into the Hint field.

Clear the check box to omit section descriptions from the knowledge portal.**Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Number of Knowledge Base items to preview in a section \(**glide.knowman.section\_limit**\)

</td><td>

Set the maximum number of articles per topic for the knowledge portal. The specific articles shown depends on the Knowledge section sort field property setting.**Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Knowledge section sort field \(**glide.knowman.section\_sort**\)

</td><td>

Select the default order for articles within each topic section on the knowledge portal.-   Published: uses the date published.
-   View count: uses the number of times articles have been viewed during the period specified in the Number of days used when summing article views property \( applicable only in Knowledge Management v2.\)
-   Alphabetically: uses the first letter of the article title \(Short description field\).

 **Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Knowledge Base section sort direction \(**glide.knowman.section\_sort\_direction**\)

</td><td>

Select the order, ascending or descending, in which articles are listed within each topic section on the knowledge portal. The value used for sorting is set in the Knowledge section sort field property. **Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Show unpublished articles in Knowledge Base portal and topic lists \(**glide.knowman.show\_unpublished**\)

</td><td>

Select the check box to allow users to see unpublished articles in the knowledge portal and knowledge search results. Use the subsequent List of roles... properties to designated which users can see articles in various unpublished states. If this is not selected, users with appropriate roles can access unpublished articles through other modules of the Knowledge Base application.

</td></tr><tr><td>

List of roles \(comma separated\) that can see articles in the Review workflow state in the Knowledge portal and Topic list \(**glide.knowman.section.view\_roles.review**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If Show unpublished articles in Knowledge Base portal and topic lists is selected, users with these roles see articles in the Review workflow state in the knowledge portal, in the topic list that appears when they click a topic title on the portal, and in knowledge search results.

</td></tr><tr><td>

List of roles \(comma separated\) that can see articles in the Draft workflow state in the Knowledge portal and Topic list \(**glide.knowman.section.view\_roles.draft**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If Show unpublished articles in Knowledge Base portal and topic lists is selected, users with these roles see articles in the Draft workflow state in the knowledge portal, in the topic list that appears when they click a topic title on the portal, and in knowledge search results.

</td></tr><tr><td>

Define roles that can view articles in other/custom workflow states \(**glide.knowman.section.view\_roles.stagesAndRoles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If Show unpublished articles in Knowledge Base portal and topic lists is selected, define the custom field and role as `workflow state:[roles];`. The users with these roles see articles in the custom workflow state on the knowledge portal.The property is not applicable to the retired knowledge articles. Only users with the knowledge\_admin role can view retired articles.

</td></tr><tr><td>

The number of articles that are asynchronously loaded when scrolling down in the new search results page \(**glide.knowman.search.articles\_per\_page**\)

</td><td>

Enter the number of articles to be displayed during a search.**Note:** This property applies only to Knowledge Management v3 pages. This property is not supported on Knowledge Management v2 pages.

</td></tr><tr><td>

Show only Knowledge topic titles on portal page \(no article links\) \(**glide.knowman.home\_titlesonly**\)

</td><td>

Select the check box to omit all article titles from the knowledge portal and show only the topic names. Users can click the topic title to see the list of related articles. **Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr id="glide-knowman-view-age-days"><td>

Number of days \(integer, default 30\) used when summing article views \(**glide.knowman.view\_age.days**\)

</td><td>

Enter a number of days to consider when calculating view count. The View count field in the Knowledge form will be updated periodically to reflect the view count based on this property. For example, if you enter 60, the view count is the total number of views in the past 60 days. Enter 0 to have ServiceNow consider all views, regardless of date. **Note:** If you edit this property, run the Count Knowledge Use scheduled job to see the changes immediately. By default, the Count Knowledge Use scheduled job runs daily and updates the view counts on the knowledge articles. To view the scheduled job, navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

 New customers as of the Paris release will not have access to the View count property and Count Knowledge scheduled job. Existing customers prior to the Paris release can continue to use the property and scheduled job.

 If you set the property value to 0:

 -   The Count Knowledge scheduled job does not run.
-   The View count of an article does not have a rolling count, the existing view count gets incremented for every article view

**Note:** Beginning Vancouver release, **glide.knowman.view\_age.days** and Count Knowledge scheduled job is deprecated. So, set the **glide.knowman.view\_age.days** to zero and do not use it.

</td></tr><tr><td>

Automatically place cursor in Knowledge portal search box \(**glide.knowman.portal\_search\_focus**\)

</td><td>

Select the check box to have ServiceNow place the cursor in the search field when a user opens the knowledge portal. Clear the check box to have users click in the search field before entering a search term. **Note:** This property applies only to Knowledge Management v2 pages. This property is not supported on Knowledge Management v3 pages.

</td></tr><tr><td>

Session level cache in "Most useful article" \(**glide.knowman.use\_session\_cache\_for\_most\_useful\_articles**\)

</td><td>

Set the property to True to enable session level cache in 'Most useful Articles' portal widget.-   Type: true \| false
-   Default value: true
-   Location: System Properties

</td></tr><tr><td>

Enable SEO for selected portal for article view page. \(**glide.knowman.serviceportal.seo\_portals**\)

</td><td>

Value contains a comma-separated list of service portal record sys\_ids. The SEO indexing of knowledge articles is enabled on the portals mentioned in the list and is blocked by the noindex metatag for other portals. If at least one portal is listed, SEO suggestions display when users author or edit knowledge articles. -   Type: string
-   Default value: none
-   Location: System Properties

 **Note:** If the property value is empty, the indexing is enabled for all portals.

</td></tr><tr><td>

Comma-separated list of service portal record sys\_ids \(**glide.knowman.serviceportal.use\_numbered\_url.portals**\)

</td><td>

Configure the property value to include sys\_id of any portal so that article URLs in portal widgets \(for example Most Useful, Featured, Most viewed articles, related article\) and search results use sysparm\_number parameter instead of sys\_kb\_id parameter.

 -   Type: string
-   Default value: None
-   Location: System Properties

 **Note:** If there are multiple portals, delimit their sys\_ids by comma \(,\).

</td></tr><tr><td>

View article as another user \(**glide.knowman.enable\_view\_as\_user**\)

</td><td>

Set the property to `true` to search and view an article as another authorized user.-   Type: true \| false
-   Default value: false
-   Location: System Properties

</td></tr><tr><td>

\(**glide.knowman.serviceportal.seo\_user\_agent**\)

</td><td>

This property contains the bots' name patterns, which are used to determine whether the user-agent is a Search Crawler bot.-   Type: string
-   Default value: None
-   Location: System Properties

</td></tr></tbody>
</table>## Knowledge search properties

Knowledge search properties give you control over the search options available to users and the presentation of search results.

**Note:** Knowledge search properties is only applicable to Zing search. To configure AI search implementation, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md).

<table id="table_cr4_tb3_54"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge search result order \(**glide.knowman.order.search**\)

</td><td>

Select the order for displaying search results:-   **Number of Views**: orders search results based on the **Number of days used when summing article views** property.
-   **Relevancy**: orders search results based on content that is similar to the search term.
-   **Last Modified**: orders search results based on modification date.

 This property is applicable for search within the Knowledge Management application and not the ServiceNow AI Platform global search.

</td></tr><tr><td>

Search method to find Knowledge articles from a task or directly in the Knowledge Base \(**glide.knowman.search.operator**\)

</td><td>

Select the search approach to use when the search term includes multiple words.-   **OR query**: returns articles that contain at least one word from the search term.
-   **AND then OR query**: first searches for articles that include all words in the search term \(an AND query\). If no matches are found, an OR query is performed.

</td></tr><tr><td>

Show author in knowledge search results \(**glide.knowman.search.show\_author**\)

</td><td>

Select the check box to include the author of each article in knowledge search results.If the article versioning feature is enabled, articles with a version number less than or equal to 1.0 display **Authored by &lt;name&gt;** and articles with a version number greater than 1.0 display **Revised by &lt;name&gt;**.

</td></tr><tr><td>

Show last modified date and time in knowledge search results \(**glide.knowman.search.show\_last\_modified**\)

</td><td>

Select the check box to show the date and time article was last edited in knowledge search results.

</td></tr><tr><td>

Show publish date in knowledge search results \(**glide.knowman.search.show\_published**\)

</td><td>

Select the check box to show the date article was published in knowledge search results.

</td></tr><tr><td>

Show category in knowledge search results \(**glide.knowman.search.show\_category**\)

</td><td>

Select the check box to show the category breadcrumbs of each article in knowledge search results.

</td></tr><tr><td>

Show number of views in knowledge search results \(**glide.knowman.search.show\_view\_count**\)

</td><td>

Select the check box to include the number of times each article was viewed in knowledge search results.

</td></tr><tr><td>

How to display attachments in Knowledge Search Results \(**glide.knowman.search.attachment**\)

</td><td>

Select the behavior of how the attachments are shown in the search results:-   **Do not show attachment**
-   **Show only link for attachment** \(default\)
-   **Show attachment with text snippet**

 For best performance, select **Do not show attachment**, or **Show only link for attachment**.

 **Note:** Starting with the San Diego release, **Show only link for attachment** is activated by default. For existing customers prior to the San Diego release, the default selection is **Show attachment with text snippet**.

</td></tr><tr><td>

Show relevancy in knowledge search results \(**glide.knowman.search.show\_relevancy**\)

</td><td>

Select the check box to show how relevant each search result is based on the search string. **Relevancy** value is only shown when knowledge search result order property is set to **Relevancy**.

</td></tr><tr><td>

Show number of knowledge blocks in the knowledge block search results when creating or updating a knowledge article \(**glide.knowman.add\_blocks.search\_results**

</td><td>

Define how many search results can be displayed when a knowledge block is searched for. By default, the minimum value is 6 and the maximum is 25.

</td></tr><tr><td>

Enable instant search results for knowledge \(**glide.knowman.search.instant\_results**\)

</td><td>

Select the check box to enable instant search for search results. The default value is set to **No**.

</td></tr><tr><td>

Show Knowledge Base name in Knowledge search results \(**glide.knowman.search.show\_knowledgebase**\)

</td><td>

Select the check box to display the knowledge base to which the knowledge article belongs. For example, **IT**.

</td></tr><tr><td>

Show average rating from knowledge search results \(**glide.knowman.search.show\_rating**\)

</td><td>

Select the check box to display the average star ratings for knowledge base articles.This property is applicable to the search results for knowledge articles that appear on the Knowledge Management Service Portal search results page and service portal widgets such as Knowledge Featured Articles and Knowledge Most Viewed Articles. For more information, see [Using search in Knowledge Management Service Portal](../concept/knowledge-service-portal-search.md) and [Configure the home page widget instance options](../task/config-homepage-widget-options.md).

</td></tr><tr><td>

Show article number in knowledge search results \(**glide.knowman.search.show\_article\_number**\)

</td><td>

Select the check box to display the article number for each article in the search result.If the article versioning feature is enabled, the article number and the version number are displayed for each article in the search result.

</td></tr><tr><td>

Specify default language for searching articles \(**glide.knowman.search.default\_language**\)

</td><td>

Set the property to the default language for searching articles. -   Type: String
-   Default value: user-specified
-   Location: System Properties

 **Note:** If the **glide.knowman.enable\_multi\_language\_search** property is set to **True**, then the multi-language search capability overrides the default language search capability.

</td></tr><tr><td>

Enable multi-language search \(**glide.knowman.enable\_multi\_language\_search**\)

</td><td>

Set the property to **True** to enable search for multiple languages simultaneously.-   Type: true \| false
-   Default value: false
-   Location: System Properties

 **Note:** If this property is set to **True**, it overrides the setting for the **glide.knowman.search.default\_language** property.

</td></tr><tr><td>

Disable Knowledge blocks feature \(**glide.knowman.blocks.enable**\)

</td><td>

Allows you to disable Knowledge blocks feature partially.-   Type: true \| false
-   Default value: true
-   Location: System Properties

 **Note:**

If the property is set to **True** and **Enable Blocks** field is selected:

-   You can create new blocks in the Knowledge Bases.
-   You can add blocks to an article in the Knowledge Bases.

If the property is set to **False**:

-   You cannot create new blocks.
-   You cannot add blocks to new or existing articles.
-   **Enable Blocks** field is inactive on the Knowledge Bases form.
-   Any existing articles with block content will continue to show the content.

</td></tr></tbody>
</table>## Knowledge article view properties

Article view properties give you control over the meta data and rating options that appear with articles. They also enable you to grant access to individual feedback options based on user role.

<table id="table_s2m_fvh_54"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show tasks to which an article has been recently attached \(**glide.knowman.recent\_tasks.display**\)

</td><td>

Select the check box to have article view include a list of tasks associated with the article. The list of associated tasks appears on the Most Recent Tasks widget on the article view page. The widget appears only when a task is attached to the article and this property is set to **Yes**. Knowledge articles can be attached to a task by clicking the **Attach to Task** button after searching from a form.

</td></tr><tr><td>

Number of attached tasks to display when viewing an article \(**glide.knowman.recent\_tasks**\)

</td><td>

Specify the maximum number of tasks to list in article view.

</td></tr><tr><td>

Show article rating section, which may optionally include yes/no rating, star rating, and flagging options \(**glide.knowman.show\_rating\_options**\)

</td><td>

Select the check box to display the rating options for users with specific roles. Clear this check box to omit the rating section for all users, regardless of role. The **Feedback** field is always displayed for all users.

</td></tr><tr><td>

List of roles \(comma separated\) that can see an article's rating section, which may optionally include yes/no rating, star rating, and flagging option \(**glide.knowman.show\_rating\_options.roles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If **Show article rating section** is selected, users with the roles listed here see the yes/no rating, star rating, and flagging options, according to related property settings. Be sure to include all roles that should be permitted to see any of these rating options. Separate properties enable you to identify specific roles for each option separately. All roles in those properties must also be listed here.

</td></tr><tr><td>

Show the "Was this article helpful?" yes/no rating option. \(**glide.knowman.show\_yn\_rating**\)

</td><td>

Select the check box to display the "Was this article helpful?" rating to users with roles set in the associated property. This appears only if the **Show article rating section** property is selected.

</td></tr><tr><td>

List of roles \(comma separated\) that can see yes/no "Was this article helpful?" rating option. \(**glide.knowman.show\_yn\_rating.roles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If both **Show article rating section** and **Show the "Was this article helpful?"** properties are selected, users with the roles listed here see the "Was this article helpful?" rating in article view. All roles listed here must also be listed in the **List of roles that can see an article's rating section** property.

</td></tr><tr><td>

Show "Create Incident" link \(**glide.knowman.create\_incident\_link.display**\)

</td><td>

Select the **Yes** check box to display the **Create Incident** link.

</td></tr><tr><td>

URL used for the "Create Incident" link \(**glide.knowman.create\_incident\_link**\)

</td><td>

Enter the URL for the page where users can create an incident only if the **Show "Create Incident" link"** property is selected.To find the URL, open the appropriate page, then right-click the header bar and choose **Copy URL**. Highlight the URL that appears and use the browser's copy and paste feature to place it into this property field.

</td></tr><tr><td>

Show five-star rating option \(**glide.knowman.show\_star\_rating**\)

</td><td>

Select the check box to display the five-star rating to users with roles set in the associated property. This appears only if the **Show article rating section** property is selected. This property is applicable to the knowledge article view page in the Knowledge Management Service Portal. For more information, see [Knowledge Management Service Portal article view page features](../concept/knowledge-service-portal-view.md).

</td></tr><tr><td>

List of roles \(comma separated\) that can see five-star rating option \(**glide.knowman.show\_star\_rating.roles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If both **Show article rating section** and **Show five-star rating option** properties are selected, users with the roles listed here see the five-star rating option in article view. All roles listed here must also be listed in the **List of roles that can see an article's rating section** property.

</td></tr><tr><td>

Show "Flag Article" option to identify incomplete/inaccurate articles \(**glide.knowman.show\_flag**\)

</td><td>

Select the check box to display the flag article option to users with roles set in the associated property. This appears only if the **Show article rating section** property is selected.

</td></tr><tr><td>

List of roles \(comma separated\) that can flag incomplete/inaccurate articles \(**glide.knowman.show\_flag.roles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If both the **Show article rating section** and **Show "Flag Article" option** properties are selected, users with the roles listed here see the flag article option in article view. All roles listed here must also be listed in the **List of roles that can see an article's rating section** property.

</td></tr><tr><td>

Show user comments on knowledge articles \(**glide.knowman.show\_user\_feedback**\)

</td><td>

Select one of the options: **When article loads** or **When user clicks link to show comments**, for the roles defined in **glide.knowman.show\_user\_feedback.roles** to be able to view the user comments. If you select **Never**, none of the roles will be able to see the comments.

</td></tr><tr><td>

List of roles \(comma separated\) that can see user comments on an article \(**glide.knowman.show\_user\_feedback.roles**\)

</td><td>

Enter role names exactly as they appear in **User Administration** &gt; **Roles**. If the **Show user comments on knowledge articles** property is selected, users with the roles listed here can add and view user comments in article view.

</td></tr><tr><td>

Maximum number of user comments displayed on a knowledge article \(**glide.knowman.feedback.display\_threshold**\)

</td><td>

Set the maximum number of user comments to display. If no value is set, all comments are displayed. This property does not apply to Live Feed comments on the article view page.

</td></tr><tr><td>

Use Live Feed for Knowledge feedback \(**glide.knowman.use\_live\_feed**\)

</td><td>

Set the property to **True** to use Live Feed to manage and display feedback on knowledge articles.-   Type: true\|false
-   Default value: false
-   Location: System Properties

</td></tr><tr><td>

Determines the maximum number of knowledge article feedbacks that user can post per day \(**glide.knowman.max\_comments\_per\_user\_daily**\).

</td><td>

Enter the value to define the maximum feedbacks per day.-   Type: integer
-   Default value:
-   Location: System Properties

 **Note:** If no value is defined, then no restrictions are applied to the number of feedbacks.

</td></tr></tbody>
</table>## Knowledge homepage properties

Knowledge homepage properties control the featured content on the knowledge homepage.

|Property|Description|
|--------|-----------|
|Display or hide the count of articles and questions in the Knowledge Homepage \(**glide.knowman.show\_number\_on\_homepage**\)|Select to display or hide the count of knowledge articles and questions on the Knowledge homepage.|
|Default keyword for getting pinned articles \(**glide.knowman.default\_keyword**\)|Enter a default keyword for pinned articles. Articles pinned with the specified keyword appear in the Featured Content section of the knowledge homepage.|
|Display or hide the count of articles and questions in the category and child categories \(**glide.knowman.show\_number\_on\_categories**\)|Select to display the count of articles and questions within each category, including subcategories, when browsing or searching knowledge bases.|
|Show Knowledge Home page when user has access to only one Knowledge Base \(**glide.knowman.show\_home\_if\_one\_kb**\)|Select to display the Knowledge homepage when the current user has access to only one knowledge base.|
|Default header title for the pinned articles section on knowledge home pages \(**glide.knowman.default\_pinned\_section\_header\_title**\)|Enter a title for the Featured Content section of the knowledge homepage.|

## Other knowledge properties

Other knowledge properties let you control general knowledge management features.

<table id="table_hcs_vc3_54"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

When attaching an article to an incident, copy the content into this field \(**glide.knowman.attach.fields**\)

</td><td>

When a user searches knowledge from a task form \(such as an incident, problem, or change\) and clicks the **Attach to Task** button for an article, the system copies the article number and content into the field specified in the **Value** column here. This field is generally a journal field such as **Comments** or **Work notes**.Use dot walking to copy the article content into related records. If a specified field does not exist, that field is ignored.

 If the property has no value, comments is used.

</td></tr><tr><td>

Displays a read-only article view page when articles are viewed from contextual search \( **glide.knowman.contextual\_search.show\_read\_only\_article**\)

</td><td>

Displays a read-only article view page when knowledge articles are viewed from contextual search.-   Type: true\|false
-   Default value: true

 **Note:** The **glide.knowman.contextual\_search.show\_read\_only\_article** property is activated by default. If the property isn’t available, add it manually and set its value to **true** to display read-only knowledge articles accessed from the contextual search. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

</td></tr><tr><td>

Knowledge Management logo to display if running out of the ServiceNow frames \(**glide.knowman.frameless\_logo**\)

</td><td>

Click the reference lookup tool ![Lookup icon](../image/Iconreferencelookup.png) and choose an image file to be displayed on knowledge pages that are used outside of the ServiceNow application frames. For example, the logo image selected here appears if you create a Content Management System site that includes knowledge pages. You can also enter the **Name** of an image stored in the database to use that image. **Note:** This property applies only to Knowledge v2 pages. This property is not supported on Knowledge v3 pages.

</td></tr><tr><td>

Hide the 'Import' functionality \(button and drag-n-drop\) for all users \(**glide.knowman.import.hide\_import\_functionality**\)

</td><td>

Select **Yes** to hide the **Import Articles** button. If you have not yet migrated to Knowledge v3 and are using legacy Knowledge v2, you can configure the visibility of the **Import Articles** button to prevent users from importing articles to knowledge bases.

</td></tr><tr><td>

Show publish check box on the knowledge import pop-up \(**glide.knowman.import.show\_publish\_checkbox**\)

</td><td>

Select **No** to remove the **Publish** check box on the knowledge import form so that an article cannot be published as part of the import process. Default is yes.

</td></tr><tr><td>

Use submission workflow \(**glide.knowman.submission.workflow**\)

</td><td>

Select the **Yes** check box to use the knowledge submission workflow instead of the standard knowledge workflow. If this option is selected, each time a user creates knowledge from an incident or problem, the content is placed into a submission record instead of a draft article. Transforming knowledge submissions into articles follows a specific workflow.

</td></tr><tr><td>

The sys\_id of the knowledge base when creating knowledge from task records \(**glide.knowman.task\_kb**\)

</td><td>

Enter the sys\_id of the knowledge base to put new knowledge articles created from tasks in.

</td></tr><tr><td>

Before displaying the text of the article in search results or the article view, check field-level ACLs on appropriate field: kb\_knowledge.text \(HTML article\) or kb\_knowledge.wiki \(wiki text article\) \(**glide.knowman.text.check\_can\_read**\)

</td><td>

Select this check box if users must have ACL-based permission to view text fields on the Knowledge \[kb\_knowledge\] table to read article previews in knowledge search results.

</td></tr><tr><td>

Defines the number of results to be considered when building the search filters \(**glide.knowman.search.facet\_depth**\)

</td><td>

Define maximum number of knowledge articles to be considered from search results for populating search filters. -   Type: string
-   Default value: 300
-   Location: System Properties

</td></tr><tr><td>

Send notification to approvers and authors in article approval workflow \(**glide.knowman.enable\_approval\_notification**\)

</td><td>

Select this check box to send approval email notifications. By default, the property is enabled.

</td></tr><tr><td>

Allow articles in the global domain to be checked out or edited by users in another domain \(**glide.knowman.allow\_edit\_global\_articles**\)

</td><td>

Enter the value as `true` to enable checking out and editing global articles for users from a domain other than the global domain.-   Type: true \| false
-   Default value: true
-   Location: System Properties

</td></tr><tr><td>

When showing a list of articles through the Knowledge portal \(using the kb\_list UI Page\), remove articles the user cannot see before building the list \(**glide.knowman.list.filter**\)

</td><td>

Enter the value as `true` to enable removal of articles that user cannot see before building the articles list in the knowledge portal. -   Type: true \| false
-   Default value: false
-   Location: System Properties

If you have large number of articles in your knowledge base, setting this property to `true` will negatively impact performance.

</td></tr><tr><td>

Create translation task when an article is published \(**glide.knowman.translation.enable\_translation\_task**\)

</td><td>

Enter the value as `true` to enable creation of translation tasks.-   Type: true \| false
-   Default value: false
-   Location: System Properties

 **Note:** When you enable this property, you can’t modify the knowledge base of existing articles.

</td></tr><tr><td>

Deny access to a knowledge base when either Can Read or Can Contribute user criteria list for the knowledge base isn't specified \(**glide.knowman.block\_access\_with\_no\_user\_criteria**\)

</td><td>

Enter the value as `true` to deny contribute access to a knowledge base when Can Contribute or Can Read user criteria isn’t set. -   Type: true \| false
-   Default value: true
-   Location: System Properties

</td></tr><tr><td>

Override contribute access based on Can Read and Cannot Read user criteria at article level \(**glide.knowman.apply\_article\_read\_criteria**\)

</td><td>

Enter the value as `true` to override contribute access to a knowledge article based on Can Read and Cannot Read user criteria at the article level. -   Type: true \| false
-   Default value: false
-   Location: System Properties

</td></tr><tr><td>

Send email notifications on the first day of each month for articles expiring in the next month \(**glide.knowman.enable\_article\_expiry\_notification**\)

</td><td>

Enter the value as `true` to send email notifications to a list of recipients about articles expiring next month on the first day of each month. The recipients list depends on the ownership group and article versioning features. For more information, see [Knowledge subscriptions](../concept/knowledge-article-subscriptions.md).-   Type: true \| false
-   Default value: false
-   Location: System Properties

</td></tr><tr><td>

Determines whether to apply ACLs on the search results \(**glide.knowman.search.apply\_acls**\)

</td><td>

Enter the value as `true` to apply knowledge ACLs on knowledge article search results. -   Type: true \| false
-   Default value: true
-   Location: System Properties

 **Note:** If the **glide.knowman.search.apply\_acls** is set to true, a knowledge base without any articles present in the search results might appear in the Knowledge Field Facet when filtering by knowledge base. For more information, see [Configure filter facet widget instance options](../task/config-search-results-filter-facets.md).

</td></tr><tr><td>

Comma separated list of all domains of office365 online sites, in which the Knowledge management Word add-in will be available \(**sn\_km\_word.glide.knowman.word.xframe**\)

</td><td>

Enter a list of all the parent domains in the Microsoft Word Online application in which Knowledge Management - Add-in for Microsoft Word is embedded. For multiple entries, separate the domains with commas.-   Type: string
-   Default value: None
-   Location: System Properties

</td></tr><tr><td>

Download the original Word document from the article view page in a portal and Workspace. Enabling the property might affect the search relevancy of the article \(**sn\_km\_word.glide.knowman.enable\_document\_download**\)

</td><td>

Enter the value as `true` to download the original Word document from the knowledge article view page in a portal and Workspace.-   Type: true \| false
-   Default value: false
-   Location: System Properties

</td></tr><tr><td>

Determines the duration required to capture the metrics \(Article Views, Portal page views, and Portal searches\). **glide.knowman.usage\_metrics\_duration**

</td><td>

Enter the value to change the duration to capture the knowledge usage metrics.-   Type: integer
-   Default value: 60
-   Location: System Properties

</td></tr><tr><td>

Translate a knowledge article from a translation task \(**glide.knowman.translation.enable\_translation\_task**\)

</td><td>

Enter the value as `true` to enable the translation.-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

Default language for searching Knowledge Articles \(**glide.knowman.search.default\_language**\)

</td><td>

Enables you to set the default language for searching articles different from the logged-in language.-   Type: string
-   Default value: None
-   Location: System Properties

 Following are the two character values to set the default searching language:

-   en - English US
-   fr - Francais
-   es - Español
-   it - Italiano
-   de - Deutsch

 To enable search for different languages simultaneously, navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Properties** &gt; **Enable multi language search** and select the check box.

**Note:** If the **glide.knowman.search.default\_language** system property is inactive, you can search one language at a time. If the property is enabled, you can search for multiple languages simultaneously.

</td></tr><tr><td>

Provides replacement article for a retired article \(**glide.knowman.enable\_article\_replacement\_on\_retire**\)

</td><td>

Enables you to provide a replacement article to a retired knowledge article. By default, the property value is set to true.-   Type: true \| false
-   Default value: true
-   Location: System Properties

</td></tr><tr><td>

Retire the knowledge block attached to an article \(**glide.knowman.allow\_retire\_block**\)

</td><td>

Enter the value as `true` to retire the knowledge block attached to an article.-   Type: true \| false
-   Default value: true
-   Location: System Properties

 **Note:** If you set the \(**glide.knowman.allow\_retire\_block**\) system property as true and if:

-   An article is associated with the knowledge block a pop-up window displays `There are articles using this block. Do you still want to retire this block?`.
-   No article is associated with the knowledge block a pop-up window displays `Are you sure you want to retire this block?`.

</td></tr><tr><td>

Determines the recommended document size \(**glide.knowman.import.max\_document\_size**\)

</td><td>

Enables you to set the recommended file size \(in megabytes\) while importing a document. By default, the value is set to 30.-   Type: integer
-   Default value: 30
-   Location: System Properties

</td></tr></tbody>
</table>## Article versioning properties

The knowledge administrator can set knowledge properties that enable users to edit specific fields on published articles without creating new versions.

The article versioning feature requires the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\). For more information, see [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md) and [Article versioning](../concept/article-versioning.md).

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable article versioning feature \(**glide.knowman.versioning.enabled**\)

</td><td>

Select the check box to enable the article versioning feature. -   Type: true \| false
-   Default value: true
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Enable minor edits to a published article without creating a new version \(**glide.knowman.versioning.enable\_minor\_edits**\)

</td><td>

Select the check box to enable minor edits to published articles and associated attachments without creating a new version.-   Type: true \| false
-   Default value: false
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

**Note:** To perform the minor edits to the published articles, the user must be the knowledge base owner or the knowledge administrator or the knowledge base manager.


</td></tr><tr><td>

A comma-separated list of fields that can be edited on published articles without creating a new version \(**glide.knowman.versioning.minor\_edit\_fields**\)

</td><td>

Enter the fields in a comma-separated list that can be edited on published articles without creating a new version.-   Type: String
-   Default value: valid\_to
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

 You can also enter the property value `attachments` to add or remove any attachments associated with a knowledge article without checking out the article.

</td></tr></tbody>
</table>## Knowledge subscription properties

The knowledge administrator can set configuration properties that enable users to subscribe to knowledge bases and knowledge articles.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable subscribe feature for KM \(**glide.knowman.enable\_km\_subscription**\)

</td><td>

Select the check box to enable the Knowledge subscription feature. -   Type: true \| false
-   Default value: true
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

List of roles \(comma-separated\) who can have subscription feature \(**glide.knowman.enable\_km\_subscription.roles**\)

</td><td>

Enter the roles in a comma-separated list that can use the Knowledge subscription feature. -   Type: String
-   Default value: knowledge
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

List of workflow states \(comma-separated\) that can have subscription feature \(**glide.knowman.enable\_km\_subscription.workflow\_state**\)

</td><td>

Enter the workflow states for knowledge articles in a comma-separated list that users can subscribe to. -   Type: String
-   Default value: draft,review,published
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Article quality index properties

The knowledge administrator can set the pass score for AQI reviews using the knowledge properties page.

<table id="table_hv5_x4r_kbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pass score for AQI reviews \(**glide.knowman.aqi\_pass\_score**\)

</td><td>

Set the pass score for AQI reviews.-   Type: Integer
-   Default value: 70
-   Range of values possible: 1-100

</td></tr><tr><td>

List of article workflow states to perform AQI reviews \(**glide.knowman.aqi.article\_workflow\_states**\)

</td><td>

Enter the article workflow states, in a comma-separated list, where users can perform AQI reviews.-   Type: String
-   Default value: draft,review,published

</td></tr></tbody>
</table>## External Content Integration Properties

Administrators can configure the properties to add allowed content types and change the UI label for the external content integration feature.

<table id="table_l4k_zbl_kbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum limit for total size of external content in Knowledge Management \(in GB\) \(**sn\_km\_intg.glide.knowman.external.max\_content\_size**\)**Note:** This is a read-only field.

</td><td>

-   Type: Integer
-   Default value: 2

</td></tr><tr><td>

Maximum size of an external article including its attachments \(in MB\) \(**sn\_km\_intg.glide.knowman.external.max\_article\_size**\)**Note:** This is a read-only field.

</td><td>

-   Type: Integer
-   Default value: 8

</td></tr><tr><td>

An editable, comma-separated list of allowed content types to be processed from the source system \(**sn\_km\_intg.glide.knowman.external.allow\_content\_types**\)

</td><td>

-   Type: Comma separated values
-   Default value:application/msword,application/vnd.openxmlformats-officedocument.wordprocessingml.document,application/vnd.ms-excel,application/vnd.openxmlformats-officedocument.spreadsheetml.sheet,application/vnd.ms-powerpoint,application/vnd.openxmlformats-officedocument.presentationml.presentation,application/pdf,text/plain,text/html,image/gif,image/jpeg,image/png
-   Other possible values: application/xml, video/mp4, audio/mpeg

</td></tr><tr><td>

List of content types not allowed to be processed from the source system \(**sn\_km\_intg.glide.knowman.external.reject\_content\_types**\)**Note:** This property is read-only and takes precedence over allowed content types.

</td><td>

-   Type: Comma-separated values
-   Default value: application/octet-stream,application/x-apple-diskimage,application/vnd.microsoft.portable-executable

</td></tr><tr><td>

UI Label for indicating external articles in Search Results and Article View Pages \(**sn\_km\_intg.glide.knowman.external.ui\_label\_for\_external\_content**\)

</td><td>

-   Type: String
-   Default value: External Content

</td></tr></tbody>
</table>## Actionable Knowledge Feedback Properties

The Knowledge administrator can set configuration properties that would create actionable feedback tasks.

<table id="table_t1z_qt4_gdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create actionable feedback task when an article is flagged.\(**glide.knowman.feedback.enable\_actionable\_feedback\_for\_flag**\)

</td><td>

Select the check box to enable actionable feedback task generation when an article is flagged for incorrect or inappropriate content.-   Type: true\|false
-   Default value: true
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Create actionable feedback task when an article is marked as not helpful \(**glide.knowman.feedback.enable\_actionable\_feedback\_for\_helpful**\)

</td><td>

Select the check box to enable actionable feedback task generation when an article is marked as not helpful.-   Type: true\|false
-   Default value: false
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Create actionable feedback task when an article is rated at or lower than this value. 0 or no value indicates that actionable feedback tasks are not enabled for Rating type feedback \(**glide.knowman.feedback.enable\_actionable\_feedback\_for\_rating**\)

</td><td>

An actionable feedback task is created when an article is rated at or lower than this value. The article is rated on a scale of 1-5.-   Type: Integer
-   Default value: none
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Create actionable feedback task only when feedback details are provided for the negative feedback \(**glide.knowman.feedback.enable\_explicit\_feedback**\)

</td><td>

Select the check box to enable actionable feedback task generation for the negative feedback.-   Type: true\|false
-   Default value: false
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

 **Note:** Set the property to **True** to deactivate feedback task generation if:

-   The feedback dialog box is close or cancel
-   Other option is chosen and no reason provided

</td></tr></tbody>
</table>## Group ownership properties

The knowledge administrator can set group ownership properties that enable the use of ownership groups for knowledge articles and decide who can edit and approve a published knowledge article.

<table id="table_mnk_g4c_54"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable ownership group for Knowledge articles \(**glide.knowman.ownership\_group.enabled**\)

</td><td>

Select the check box to enable associating ownership groups with knowledge articles.**Note:** Once you have set this property to **true**, try not to change it to **false**. Before setting this property back to **false**, manually reassign all knowledge articles associated with any ownership group, close all article approvals sent to ownership groups, and resolve all open feedback tasks assigned to ownership groups.

 -   Type: true \| false
-   Default value: false
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Retain contribute access for author or reviser of knowledge article linked to ownership group \(**glide.knowman.ownership\_group.override**\)

</td><td>

Select the check box to enable the author and reviser of a knowledge article to retain contribute access to the article even when an ownership group is associated with the article.-   Type: true \| false
-   Default value: false
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Allow approval of self-authored article as ownership group member \(**glide.knowman.ownership\_group.allow\_self\_approval**\)

</td><td>

Select the check box to allow ownership group members to approve self-authored articles for publication.-   Type: true \| false
-   Default value: true
-   Location: **Knowledge** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>