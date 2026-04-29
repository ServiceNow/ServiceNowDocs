---
title: Configuring Knowledge Management
description: Plan and configure your Knowledge Management implementation.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Knowledge Management

Plan and configure your Knowledge Management implementation.

## Configuration overview

Visit the following page on the ServiceNow Community for information on setting up Knowledge Management: [Knowledge Management Getting Started](https://www.servicenow.com/community/knowledge-management-articles/knowledge-management-getting-started/ta-p/2533067).

You can also use Knowledge Management capabilities within a website built on Adobe Experience Manager \(AEM\). For more information, see [Integration with Adobe Experience Manager](https://www.servicenow.com/docs/access?context=aem-integration&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Using guided setup to implement Knowledge Management

Guided setup provides a sequence of tasks that help you configure Knowledge Management on your instance. To open guided setup for Knowledge Management, navigate to **Knowledge** &gt; **Administration** &gt; **Guided Setup**. For more information, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

-   **[Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md)**  
Activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) to enable advanced features for Knowledge Management.
-   **[Knowledge Management setup guide for admins](../reference/setup-knowledge-admin.md)**  
Before users in your organization can start creating knowledge bases and knowledge articles, you must set up Knowledge Management. Work with stakeholders to define requirements for setting up Knowledge Management effectively to meet the needs of users.
-   **[Knowledge base setup guide for knowledge admins and managers](../reference/set-up-knowledge-admin-user.md)**  
After basic Knowledge Management setup is completed, you can set up a knowledge base for users to create and publish knowledge articles.
-   **[Activate the sitemap configuration and definition records for the Knowledge Portal](../task/config-sitemap-generator.md)**  
Include knowledge articles in your sitemap by activating the sitemap configuration and definition records.
-   **[Activate the knowledge management internationalization plugin](c_ActKMIntPlugin.md)**  
To enable translation of knowledge articles, you must activate multiple plugins.
-   **[Activate knowledge blocks](../task/activate-knowledge-blocks.md)**  
You can activate knowledge blocks \[com.snc.knowledge\_blocks\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Enable knowledge blocks for each knowledge base](../task/enable-knowledge-blocks-for-knowledge-base.md)**  
Enable the knowledge blocks feature for each knowledge base where you plan to use the blocks. Once enabled, you can create knowledge blocks to add to knowledge articles within a knowledge base.
-   **[Configure translation management](configure-translation-management.md)**  
Configure translation management to create translation tasks.
-   **[Activate Knowledge Management KCS Capabilities](../task/activate-kcs-capabilties-plugin.md)**  
You can activate the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) to enable the use of certain KCS roles and KCS article states.
-   **[Enable languages for a knowledge base](../task/enable-language-for-knowledge-base.md)**  
Select the languages you want enabled at a knowledge base level. Users can then create articles only for selected languages.
-   **[Configure the Knowledge Management Service Portal](knowledge-management-service-portal.md)**  
The Knowledge Management Service Portal enables users to perform the same operations that are available with the Knowledge Management V3 plugin. From the portal, users can view knowledge bases and articles, search for information, sort and filter search results, and provide feedback.
-   **[Create a knowledge base](../task/create-a-knowledgebase.md)**  
Create a knowledge base to provide a self-service platform for users to store, share, and manage content. Configure knowledge bases into product or service categories and manage user access based on permissions. Customize workflows for publishing and retiring articles in the knowledge base.
-   **[Configure knowledge bases for a portal](../task/enable-search-on-all-kb.md)**  
Select which knowledge bases are displayed in a portal to view the associated knowledge articles. If no knowledge bases are configured, users can view articles from all knowledge bases in the portal.
-   **[Configure knowledge subscriptions](../task/configure-subscription-properties.md)**  
Configure knowledge subscriptions by activating the Knowledge Management Advanced plugin and setting the subscription properties.
-   **[Configuration tasks for knowledge managers](c_KnowledgeManager.md)**  
Having multiple knowledge bases allows an organization to spread management responsibilities across multiple users, known as knowledge managers.
-   **[Configure Self-Service Analytics](../task/config-ssa.md)**  
Configure the Self-Service Analytics framework so you can use the generated metrics in a dashboard.
-   **[Managing access to knowledge bases and knowledge articles](user-access-knowledge.md)**  
Determine whether certain users or categories of users can access knowledge bases and knowledge articles by controlling contribute and read access.
-   **[User criteria diagnostics for Knowledge Management](diagnose-knowledge-user-criteria.md)**  
Manage user access to a knowledge base or an article using user criteria diagnostics. Understand what access users have to a knowledge base or an article and determine which user criteria define those permissions.
-   **[Configure knowledge article templates](configure-knowledge-article-templates.md)**  
Configure knowledge article templates to customize and display content as per your requirements.
-   **[Integration with external knowledge sources](knowledge-external-content-integration.md)**  
Use the external content integration feature to integrate content from various external sources and enable unified knowledge search results.
-   **[Duplicate knowledge article numbers](../reference/knowledge-article-duplicate-numbers.md)**  
Importing knowledge articles into an instance can create articles with duplicate numbers.
-   **[Create a custom knowledge homepage](../task/t_CreateACustomKnowledgeHomepage.md)**  
As a system administrator, you can create a module allowing users to open a knowledge homepage for a specific knowledge base or category.
-   **[View knowledge logs](../task/view-knowledge-logs.md)**  
Knowledge logs display information about which users have viewed knowledge articles, what they looked for, and where.
-   **[Use extension points for Knowledge Management](../task/extension-points-km-plugins.md)**  
Use UI extension points to add knowledge article headers and footers to knowledge articles and to customize the email template for notifications when a knowledge article is commented on. Use scripted extension points to customize the feedback object used in the email template for notifications when a knowledge article is commented on.
-   **[Train the similarity solution for Knowledge Management to find related articles](../task/train-similarity-solution-km.md)**  
Train the Knowledge Similar Articles solution definition included within the Predictive Intelligence for Knowledge Management capability to find related knowledge articles when creating or viewing a knowledge article.
-   **[Enable actionable knowledge feedback](../task/configure-act-know-feedback-properties.md)**  
The actionable knowledge feedback feature is available when the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\) plugin is activated and the actionable knowledge feedback properties are enabled.
-   **[Enable creating an article from a customer service case](administer-create-article-from-case.md)**  
You can enable authors to reuse information in a case by copying case details into an article template. Use the pre-defined customer service source case table to article template target table configuration or create custom configurations between the two tables to copy information from a case to an article.
-   **[Configuration tasks for knowledge demand insights](configuration-tasks-for-knowledge-demand-insights.md)**  
Review the following configurations tasks for knowledge demand insights.

**Parent Topic:**[Knowledge Management](knowledge-management.md)

