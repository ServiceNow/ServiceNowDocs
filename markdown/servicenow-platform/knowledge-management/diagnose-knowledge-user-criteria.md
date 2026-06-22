---
title: User criteria diagnostics for Knowledge Management
description: Manage user access to a knowledge base or an article using user criteria diagnostics. Understand what access users have to a knowledge base or an article and determine which user criteria define those permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/knowledge-management/diagnose-knowledge-user-criteria.html
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# User criteria diagnostics for Knowledge Management

Manage user access to a knowledge base or an article using user criteria diagnostics. Understand what access users have to a knowledge base or an article and determine which user criteria define those permissions.

User access to a knowledge base or an article can be restricted based on:

-   Domain separation
-   Access control list \(ACL\) rules
-   [Knowledge workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/knowledge-management/r_KnowledgeWorkflows.md)
-   User criteria set for a [knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/knowledge-management/t_SelectUserCriteria.md) or an [article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/knowledge-management/t_SelectUCArticle.md)

This feature considers domain separation and user criteria to determine the user access to knowledge bases and articles.

## Activation information

The user criteria diagnostics feature is activated with the Knowledge Management v3 plugin \(com.snc.knowledge3\). For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/t_ActivateAPlugin.md).

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/knowledge-management/knowledge-service-portal-pages.md).

