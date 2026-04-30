---
title: Control access at the knowledge base level through user criteria
description: You specify user criteria for a knowledge base to control which users are granted access to read and contribute knowledge articles to that knowledge base.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing access to knowledge bases and knowledge articles, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Control access at the knowledge base level through user criteria

You specify user criteria for a knowledge base to control which users are granted access to read and contribute knowledge articles to that knowledge base.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin, or admin

**Note:** To administer a scoped knowledge base, you must have the application-specific admin role in addition to the knowledge\_admin or admin role. For more information, see [Scoped knowledge bases](../concept/scoped-knowledge-base-administration.md).

## About this task

You can assign user criteria to control read or contribute access. For example, you could enable all users in your Support department to have contribute access to a knowledge base by creating a user criteria record with the required department set to Support, and then including the user criteria record in the Can Contribute user criteria. For more information, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md). Try to use only user criteria, which were introduced in Knowledge Management v3, to control access to knowledge bases. Roles were used for this purpose in Knowledge Management v2.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in a future release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers beginning with the Madrid release. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Click the link to knowledge base you manage.

3.  Add user criteria to the knowledge base.

    1.  Depending on the user criteria you want to set, select one or more of the relevant related lists.

        |Related list|Description|
        |------------|-----------|
        |Can Read|Users can read knowledge articles in the knowledge base.|
        |Cannot Read|Users can't read knowledge articles in the knowledge base.|
        |Can Contribute|Users can create, modify, and retire knowledge articles in a knowledge base. Contribute access to a knowledge base also provides read access to all articles in the knowledge base.|
        |Cannot Contribute|Users can't create, modify, retire, or read knowledge articles in the knowledge base.|

        **Note:** If the related lists aren't visible, configure the Knowledge form to display them. For more information, see [Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    2.  In the selected related list, add the required user criteria.

        -   As a user with the admin role, to add a new user criteria record, click **New**, specify the required fields, and then click **Submit**.
        -   As a user with the knowledge\_manager, knowledge\_admin, or admin role, to add an existing user criteria record, click **Edit**, move the required user criteria from the **Collection** column to the **Knowledge** column, and then click **Save**.
4.  On the Knowledge Base form, click **Update**.


## What to do next

After you add user criteria, you can use the user criteria diagnostics feature to verify the access that users have to a knowledge base or a knowledge article. For more information, see [User criteria diagnostics for Knowledge Management](../concept/diagnose-knowledge-user-criteria.md).

**Important:** After making user criteria additions or changes, you may need to log out and log back in to clear the prior configuration.

**Parent Topic:**[Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md)

**Related topics**  


[Create a knowledge base](create-a-knowledgebase.md)

[Create user criteria for controlling access to knowledge bases and articles](create-user-criteria-record-in-knowledge-management.md)

[Control access at the knowledge article level through user criteria](t_SelectUCArticle.md)

