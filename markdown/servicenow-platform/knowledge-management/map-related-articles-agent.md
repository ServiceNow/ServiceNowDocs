---
title: Map a related article in Agent Workspace
description: Discover similar information across articles on a topic while viewing a knowledge article. You can manually map related articles or have the application automatically present related articles using machine learning \(ML\) algorithms.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Map a related article in Agent Workspace

Discover similar information across articles on a topic while viewing a knowledge article. You can manually map related articles or have the application automatically present related articles using machine learning \(ML\) algorithms.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article for which you want to add related articles.

Role required: agent\_workspace\_user

## About this task

If you have manually mapped related articles when editing an article in Agent Workspace, those articles are listed in the Related Articles section on the knowledge article view page in the Knowledge Management Service Portal before the related articles that are predicted thorough the Knowledge Management similarity solution.

**Note:** An administrator can train the solution definition for Knowledge Management within the Predictive Intelligence feature to find related articles. For more information, see [Train the similarity solution for Knowledge Management to find related articles](train-similarity-solution-km.md).

This task provides steps to manually map related articles when editing an article in Agent Workspace. You can also manually map related articles when editing an article from the Knowledge Management application in the ServiceNow AI Platform interface. For more information, see [Map related articles](map-related-articles.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **All Articles**.

3.  Click the link to the knowledge article for which you want to map related articles.

4.  In the Related Articles related list, click **New**.

5.  On the Related Articles form, fill in the fields.

<table id="table_kn2_2bn_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to enable the mapping to the related knowledge article.

</td></tr><tr><td>

Related knowledge article

</td><td>

Knowledge article that contains related information.You can click the search for record icon \(![Search for Record icon](../image/lookup-icon.png)\), to access the list of available knowledge articles.

</td></tr><tr><td>

Knowledge article

</td><td>

Number of the knowledge article for which you are adding the related knowledge article.

</td></tr><tr><td>

Order

</td><td>

Order in which you want the article to appear in the Related Articles section on the Knowledge Management article view page. A lower value means that a knowledge article has the greater priority to appear in the Related Articles section. The default value is 100.

</td></tr></tbody>
</table>6.  Click **Save**.


## Result

The mapped articles are available in the Related Articles section on the Knowledge Management article view page in the Knowledge Management Service Portal. See [Knowledge Management Service Portal article view page features](../concept/knowledge-service-portal-view.md).

**Note:** Because system administrators can configure the number of knowledge articles shown in the Related Articles section, not all mapped related articles might appear in the Related Articles section. For more information, see [Configure knowledge related articles widget instance options](configure-related-articles-widget.md).

**Related topics**  


[Edit a knowledge article in Agent Workspace](edit-article-workspace.md)

