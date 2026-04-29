---
title: Configure access to knowledge bases for unauthenticated users
description: Identify knowledge bases accessible to unauthenticated users based on the user criteria and the system property settings.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User criteria diagnostics for Knowledge Management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure access to knowledge bases for unauthenticated users

Identify knowledge bases accessible to unauthenticated users based on the user criteria and the system property settings.

## Before you begin

You must activate the Knowledge Management v3 plugin \(com.snc.knowledge3\).

Role required: knowledge\_manager, knowledge\_admin, or admin

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **User Criteria Diagnostics**.

2.  Click the **View knowledge bases accessible to unauthenticated users** related link.

3.  Review knowledge bases accessible to unauthenticated users.

4.  Restrict unauthenticated users to access a knowledge base by selecting the knowledge base and configuring its access settings.

    -   Use user criteria to determine access to the knowledge base for unauthenticated users.

        For more information, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md).

    -   If no user criteria is specified for the knowledge base, as an administrator, you can set the value of the **glide.knowman.block\_access\_with\_no\_user\_criteria** system property to **true**.

        For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).


**Parent Topic:**[User criteria diagnostics for Knowledge Management](../concept/diagnose-knowledge-user-criteria.md)

