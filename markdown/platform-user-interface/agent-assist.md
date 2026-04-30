---
title: Finding solutions by using Agent assist
description: Find the information that you need to resolve issues by using the Agent assist search engine.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Responding to issues in an open record in Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Finding solutions by using Agent assist

Find the information that you need to resolve issues by using the Agent assist search engine.

Agent assist appears in the Contextual side panel by default and when you select the graduation cap icon \(![Agent Assist icon.](../image/knowledge-base-icon.png)\). It's possible for you to have icons for more than one Agent assist search engines. If so, each one would search a different set of information sources.

When you open a record, Agent assist automatically does a search based on a field in the open record. The field value used for the search term is configurable by your administrator but it's typically the value for the record's short description field.

The following example shows the search results for the short description "HDMI port is not working." The search results return as cards. In the following example, the card returned links to an article with the title "HDMI port is not working on my PC" and that was search was last updated 14 days ago. In the following example, you see two different colored graduation caps, which means that the Agent assist search engines are available.

![Agent Assist.](../image/agent-assist-mult-icons.png)

The default number of search results is 10. If more than 10 results are displayed, that number appears as **10+**.

Agent assist is preconfigured to search the Incident, Problem, Change, Knowledge, and Case tables for solutions. Your administrator can configure Agent assist to search the additional information sources, such as the service catalog.

You can use Agent assist in the following ways to find solutions to the record that you opened:

-   Select a card to go to the search result.

    The search result might provide the answer you need, which you can then send to the requester by using the Compose editor in Activity stream.

-   Enter a new search term in the search field next to the search icon \(![Search icon.](../image/magnifying-glass.png)\) to get different search results.

    If the search results that automatically appear don't show relevant results, enter a new search term to get better search results.

-   Filter the search results.

    By default, Agent assist returns the search results from all of its information sources. You may get too many results though. To see the search results from a subset of those information sources, select the configuration icon \(![Configuration icon.](../image/icon-configuration.jpg)\) and then select an information source.

    ![Agent assist filters.](../image/agent-assist-configuration.png)

-   Send a solution to the requester by selecting a link in the card.

    The following example shows the **Link to Problem** link, that, when selected, adds the link to a similar problem in the Compose editor that you can then send to the requester. For more information, see [Compose editor](communicating-with-requesters.md).

    ![Link to problem included.](../image/agent-assist--with-message.png)

-   If the card is an article, select the card and then select the **Attach** link to send the article to the requester.

    For more information, see [Send an article to a requester](../task/add-article-agent-assist.md).

-   If the card links to an item in the service catalog, select the card to order the item.

    For more information, see [Order a catalog item for a requester](../task/order-catalog-item-agent-assist.md).

-   Select a different Agent assist icon and repeat the search.

    If you have more than one Agent assist search engine in the Contextual side panel, each one searches through a different set of information resources. Your administrator configures the icon to click for additional Agent assist search engines.

-   If your administrator enables **Search as** on your instance, you can change the search results by changing the field values in the form pane.

    On the **Details** tab, you may be able to replace the value for **Caller**, to change the search results that are based on that value. For example, if you create cases on behalf of a customer or employee, when you enter a customer's identity in the **Caller** field in the form pane returns Agent assist search results, fsuch as 401k information, that match the customer instead of you.

-   Place a catalog order by selecting a catalog item that is shown on a card.
-   Add a knowledge article to the Compose editor by selecting the **Attach** icon \(![Attach icon.](../image/attach-icon.png)\) in Agent assist.

## No search term

Your administrator can configure Agent assist to conduct a search without using a search term. The search result is all the records from a particular information source, such as employee records. You then can get the record of a particular employee by entering the employee's name in the search field.

