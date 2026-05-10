---
title: User criteria diagnostics for Knowledge Management
description: Manage user access to a knowledge base or an article using user criteria diagnostics. Understand what access users have to a knowledge base or an article and determine which user criteria define those permissions.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# User criteria diagnostics for Knowledge Management

Manage user access to a knowledge base or an article using user criteria diagnostics. Understand what access users have to a knowledge base or an article and determine which user criteria define those permissions.

User access to a knowledge base or an article can be restricted based on:

-   Domain separation
-   Access control list \(ACL\) rules
-   [Knowledge workflows](../reference/r_KnowledgeWorkflows.md#)
-   User criteria set for a [knowledge base](../task/t_SelectUserCriteria.md) or an [article](../task/t_SelectUCArticle.md)

This feature considers domain separation and user criteria to determine the user access to knowledge bases and articles.

## Activation information

The user criteria diagnostics feature is activated with the Knowledge Management v3 plugin \(com.snc.knowledge3\). For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](knowledge-service-portal-pages.md).

-   **[Diagnose user access to a knowledge base](../task/diagnose-access-criteria-at-kb-level.md)**  
Identify which users have access to a knowledge base and what enables that access.
-   **[Diagnose user access to an article](../task/diagnose-access-criteria-at-an-article-level.md)**  
Identify which users have access to an article and what enables that access.
-   **[Configure access to knowledge bases for unauthenticated users](../task/configure-unauthenticated-user.md)**  
Identify knowledge bases accessible to unauthenticated users based on the user criteria and the system property settings.
-   **[Collect knowledge usage metrics](../task/Guest-user-diagnostic.md)**  
Capture metrics such as article views, page views, and portal searches to track aggregated knowledge usage by users.

**Parent Topic:**[Configuring Knowledge Management](configuring-knowledge-management.md)

