---
title: Managing contextual search
description: Contextual search provides a way to display results that can be relevant to the issue for which you are creating an incident or requesting a service.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing contextual search

Contextual search provides a way to display results that can be relevant to the issue for which you are creating an incident or requesting a service.

The section covers topics that help you to:

-   Understand the actions that are taken on the search results.
-   Use contextual search results in a record producer within the Service Portal or as an agent in a form.

-   **[Set a search context as default](../task/set-a-contextual-search-as-default.md)**  
If you use the contextual search REST API and don't specify which search context to use, the API uses the search context that you have set as default. The search context that you use in the API takes preference over the one marked as default.
-   **[Set the default source for search context](../task/set-source-search-context.md)**  
You can decide which source to set as the default search source.
-   **[View a searcher](../task/t_ViewASearcher.md)**  
View the details of a searcher to know which search resources it searches and which search contexts use it.
-   **[Show the related search box in a form](../task/show-related-search-box-from-form.md)**  
Enable agents to search for related content without having to modify the text in the **Short description** field.
-   **[Add multiple search fields for contextual search](../task/add-multiple-search-fields.md)**  
Add multiple search fields if you want to search from a field other than the short description without using the related search box.
-   **[Add additional resources to the source selector of a form](../task/add-addi-resource-to-source-list.md)**  
Add additional resources when you want the user to search beyond Knowledge and Service Catalog search resources. For example, add additional resources for **Open Incidents**, **Resolved Incidents**, or **Similar Open Incidents**.
-   **[Edit search resource display field record](../task/edit-addi-resources-field.md)**  
Use the search result display fields to provide titles, descriptions, and additional details for contextual search results.
-   **[Specify fields for the Cxs\_popup view](../task/def-fields-addi-resource-preview.md)**  
Edit the Cxs\_popup view to specify the fields to be shown for addition resources in the preview window of a task record. The preview helps you with the summary of the record.
-   **[Modify or disable search actions available for contextual search](../task/modify-search-actions-avail-for-cxs.md)**  
Modify or disable search actions to restrict the actions that a user can perform on a search result.
-   **[Enable viewing of search results for the current and another selected user](../task/t_SearchAsDifferentUser.md)**  
Enable the search as functionality when you want the ability to view search results common to the current user and another user that you specify.
-   **[Define contextual search for record producer](../task/t_CntxtSearchRP.md)**  
Define a record producer to trigger a search based on the text that you enter in a variable field. Search results appear at the bottom of the record producer form.
-   **[Define email configuration for contextual search](../task/define-email-configuration-for-cxs.md)**  
Define email configurations to allow the system to include search results with an email notifications.
-   **[Edit an email notification for the search results](../task/t_ConfigureAnEmailNotification.md)**  
Include search results in an email notification sent to users.
-   **[Attach a Knowledge article](../task/t_AttachAnArticle.md)**  
Attach a Knowledge article to an incident to solve issues quickly by going through the in-depth troubleshooting steps and other detailed information in the article.
-   **[Feedback information on contextual search](../reference/r_QueryFeedbackInformation.md)**  
When a user clicks any of the action buttons such as **This helped**, **Order**, or **Attached**, the feedback information is stored in specific tables. The information helps you to understand the effectiveness of the searches. You can also create custom reports by querying these tables.

**Parent Topic:**[Contextual search](c_ContextualSearch.md)

