---
title: Improving the user experience with AI Search
description: Virtual Agent uses the ServiceNow AI Platform AI Search application to return search results in bot conversations as a fallback when there are no relevant topics to display to end users. Virtual Agent also provides a Run AI Search topic block that topic authors can use to generate search results in a topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [AI Search, Virtual Agent, ServiceNow AI Platform, User experience]
breadcrumb: [Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Improving the user experience with AI Search

Virtual Agent uses the ServiceNow AI Platform® AI Search application to return search results in bot conversations as a fallback when there are no relevant topics to display to end users. Virtual Agent also provides a Run AI Search topic block that topic authors can use to generate search results in a topic.

## How Virtual Agent uses AI Search

The AI Search application, which is included with the ServiceNow AI Platform, provides relevant search results for queries and uses Machine Learning to continuously improve search results based on end-user selections. To learn more about AI Search, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

In addition to normal search results, AI Search can display Genius Result cards that show relevant catalog items, questions and answers \(Q&amp;A\), and people \(user\) information. To learn more, see [Genius Results](https://www.servicenow.com/docs/access?context=genius-results-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Catalog Genius Results and Q&amp;A Genius Results are automatically activated in the base system.

Virtual Agent uses AI Search to provide the following:

-   The Run AI Search topic block, which calls the AI Search application in a conversation. Topic designers can add this block as a topic node, to generate and display search results in a conversation. For details about the Run AI Search block and other topic blocks provided with Virtual Agent, see [Virtual Agent pre-built topic blocks for NLU](../reference/va-platform-topicblocks.md).
-   The AI Search Fallback setup topic that generates search results for end users when Virtual Agent can't determine an intent and topic or the keyword to display the appropriate conversation for user requests.

Virtual Agent provides base system \(default\) AI Search configurations that determine how search results are generated and displayed:

-   Search application configuration that defines:
    -   Index sources - Data sources to be used for search, such as catalog items or knowledge base \(KB\) articles.
    -   Search profile - Index source to be used and the type of results to show in Genius Result cards.
-   Entity View Action Mapping \(EVAM\) configuration that defines how search results and Genius Results are displayed.

The Virtual Agent search configurations are part of the default chat experience set in Assistant Designer, through the Custom Greetings and Setup feature. Use this feature to specify the context for running Virtual Agent. The chat experience defines the setup topics used in Virtual Agent conversations and the search configuration that controls the AI Search experience. The AI Search Fallback setup topic controls the AI Search experience. For details, see [Customizing a Virtual Agent chat experience](va-conversation-settings.md).

Virtual Agent and Virtual Agent Lite use AI Search functionality. If you're a Virtual Agent Lite admin, you can deactivate setup topics such as the AI Search Fallback setup topic, but you can't change the Virtual Agent search configurations set in chat experiences, the Run AI Search topic block, nor the AI Search Fallback setup topic.

In order to use AI Search in Virtual Agent, you must request it for your instance. For more information, see [Activate AI Search for Virtual Agent](../task/activate-ai-search-va.md).

## When Virtual Agent uses AI Search fallback

Virtual Agent uses AI Search fallback in the following instances:

-   Topic discovery can't find any matching topics for the user query.

    **Note:** If you're using pre-built NLU conversations, such as ITSM Virtual Agent conversations, topic discovery finds the topics that match the keywords or intents provided with those conversations, before falling back to AI Search. If your users select **Ask something else** after suggested topics are displayed, Virtual Agent takes the additional input and reruns topic discovery AI Search to return relevant search results.

-   Topic discovery returns too many topics for the user query. In this case, Virtual Agent can't determine the best topic to display to the end user.
-   Topic suggestions are displayed to the user, but the user selects the **Ask something else** option.

**Note:** If you deactivate the AI Search Fallback setup topic in a chat experience, the Virtual Agent runs the Fallback setup topic when it can't find a matching topic.

## What the AI Search results look like

In Virtual Agent, the default chat experience or a custom chat experience determines the search experience, namely the search profile used and the format of the AI Search results displayed:

-   The search application specified in the Virtual Agent default or custom chat experience defines certain aspects of the search experience, such as the search sources \(searchable content\) and synonyms used to improve search recall.
-   The EVAM configuration for Virtual Agent controls the Genius card content presented in search results \(Q&amp;A, Catalog, and People\). For information on how EVAM works, see [Exploring Entity View Action Mapper](https://www.servicenow.com/docs/access?context=exploring-entity-view-action-mapper&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

The default AI Search results include these items:

-   **Genius Result cards**

    When AI Search generates a match \(result\) with a high confidence score, Virtual Agent displays a single Genius card with the result. The cards display information returned from AI Search:

    -   Q&amp;A - Provides an answer snippet from the Knowledge Base article determined as the top search result.
    -   Catalog items - Returns the most relevant catalog item with the related entities \(catalog item name and catalog item category\).
    -   People - Returns the relevant person with the related entities \(name, department, city\).

        **Note:** The default search application for Virtual Agent is configured to include Q&amp;A \(Knowledge Base\) and Catalog results, but not People card results. The People card is not available with the default Virtual Agent search application. People card results are available if you're using the Employee Service Center \(ESC\) app and the ESC search profile, which can be specified in a Virtual Agent chat experience for ESC.

    ![Question and Answer genius card, Catalog item genius card, and People genius card](../images/genius-card-examples2.png "Genius card examples")

-   **List output**

    After a Genius Result is returned, users can indicate what they would like to do next. If they choose the option **Show me more on &lt;search item&gt;**, Virtual Agent displays search results as a list output, which includes:

    -   Knowledge articles
    -   Catalog items
    -   People
    -   Other - Generic results determined by EVAM, for example results from Microsoft SharePoint or Microsoft OneDrive connectors
    Admins can edit the prefix of these search result titles by navigating to EVAM and searching for Virtual Agent templates. Select the template for the applicable search result type and update the value for the **key** attribute. ![Virtual Agent Catalog Search Template view, with prefix codeblock highlighted.](../images/ai-search-prefix.png)

    Admins can expand the number of search results displayed up to 10, using the **com.glide.cs.ai\_search.max\_regular\_result** property. In order for the search results to display as expected, the search result limit in the search application configuration should be greater than or equal to the **com.glide.cs.ai\_search.max\_regular\_result** system property.

    **Note:** When admins specify 10 for the maximum regular results, 12 choice options display \(10 results plus the actions “I need more help” and ”Ask something else”\). However, the default total number of list options allowed on the chat widget is 10. In order for all 12 choices to display, the admin must adjust the **com.glide.cs.picker\_page\_limit** system property accordingly. For optimal user experience, fewer list options are recommended.

    Users can select a search result from the list and continue the Virtual Agent conversation. For example, when a user selects a catalog item from the search results list, Virtual Agent provides an option to request the item directly from the chat.

    ![The user selected Adobe Creative Cloud in the catalog. Virtual Agent asks, "What would you like to do now?" The user responds, "Request this item."](../images/ai-search-convo.png)

-   **Portals that display AI Search links**

    Links in the Genius card and multi-link output search results are opened automatically in a portal that you can set in various ways. For example, you can use default or custom URL mappings to specify the portal in which links are opened. To learn more, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).


## Custom search experiences

You can customize the AI Search experience in a conversation, for example to run searches that return results relevant to a particular business application. To control the AI Search results returned in a conversation, you can create a search application configuration that defines the search experience used by the AI Search topic block. For details, see [Create a custom AI Search experience for Virtual Agent conversations](../task/create-va-aisearch-application.md).

-   **[Activate AI Search for Virtual Agent](../task/activate-ai-search-va.md)**  
Once activated, AI Search configurations that are part of the Virtual Agent default chat experience become available. The AI Search Fallback setup topic controls the AI Search experience.
-   **[Create a custom AI Search experience for Virtual Agent conversations](../task/create-va-aisearch-application.md)**  
Define a custom AI Search experience in a conversation using the AI Search topic block. You create a Search Application Configuration used by the topic block to control the AI Search results returned in the conversation. Or you can use the Search Application Configuration to control AI Search results in a custom chat experience.

**Parent Topic:**[Exploring other Virtual Agent features](exploring-other-vad-features.md)

