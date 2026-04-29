---
title: Using the homepage of Knowledge Management v3
description: The Knowledge Management v3 homepage displays knowledge articles organized by knowledge base and category, as well as featured content and popular articles.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using the homepage of Knowledge Management v3

The Knowledge Management v3 homepage displays knowledge articles organized by knowledge base and category, as well as featured content and popular articles.

To view the default knowledge homepage, navigate to **Self-Service** &gt; **Knowledge**.

**Note:**

-   The knowledge homepage is not compatible with Internet Explorer 9 or earlier. Using one of these browsers will cause you to be redirected to the legacy knowledge portal.

-   The Knowledge v3 home page is not customizable. Use the [Knowledge Management Service Portal](knowledge-management-service-portal.md) for an easily configurable user experience.

-   Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](knowledge-service-portal-pages.md).


If you access knowledge from a service management application, the knowledge homepage for the associate application opens.

Only published and not yet expired knowledge articles \(that is the valid do date not yet reached\) appear on the homepage.

From the homepage, you can import a Word document to a knowledge base by clicking **Import Articles**.

**Note:** From Madrid, you can import a word document from the Import Articles module available in the Application Navigator. This feature is active by default for customers on Madrid and later releases. Existing customers on release versions prior to Madrid use the Word import functionality on the Knowledge V3 homepage. Upgrade customers use the Word import functionality on the Knowledge V3 homepage by default. If required, add the Import Articles module to the Application Navigator. If you add the module, the **Import Articles** button does not appear on the Knowledge v3 homepage.

You can also create a new article using the **Create An Article** button.

-   [Import a Word document](../task/t_ImportADocument.md)
-   [Create a knowledge article from an incident in Service Operations Workspace](../task/create-knowledge-article.md)

**Note:** You must have contribute access to at least one active knowledge base, otherwise these buttons do not appear. See [Configuration tasks for knowledge managers](c_KnowledgeManager.md).

You can select a knowledge base to browse articles within that knowledge base. You can view only knowledge bases you can access.

Articles are organized by category or by tag. Categories are listed alphabetically. You can sort content by most recent update or by number of views.

You can comment on an article. There is no HTML formatting available for comments on the Knowledge V3 homepage.

Existing customers on release versions prior to New York can view knowledge article feedback comments in the following ways.

-   On the Knowledge v3 homepage.
-   If the Knowledge Management — Service Portal plugin \(com.snc.knowledge\_serviceportal\) is installed, on the Knowledge Service Portal.
-   If the Use Live Feed for knowledge feedback property is active, in the Live Feed.

For new customers on New York and later releases, comments can only be viewed in the Knowledge Service Portal.

An administrator can configure the knowledge homepage to display the number of articles within each category. This count includes articles from subcategories. To display the article count, set the **glide.knowman.show\_number\_on\_categories** property to `true`.

-   **[Search using Knowledge Management v3](../reference/r_KnowledgeSearch.md)**  
Search for knowledge articles from the knowledge homepage using the search bar on the Knowledge Management v3 homepage.
-   **[Import a Word document to a knowledge base using Knowledge Management v3](../task/t_ImportADocument.md)**  
Import a Microsoft Word document using Knowledge Management v3 homepage to create a knowledge article.

**Parent Topic:**[Using Knowledge Management](using-knowledge-management.md)

**Related topics**  


[Define a knowledge article category](../task/t_DefineAKnowledgeCategory.md)

[Import a Word document to a knowledge base using Knowledge Management v3](../task/t_ImportADocument.md)

[Import a Word document to a knowledge base](../task/import-word-platform.md)

