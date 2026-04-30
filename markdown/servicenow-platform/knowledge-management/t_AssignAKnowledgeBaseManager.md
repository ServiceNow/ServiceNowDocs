---
title: Assign a knowledge base manager
description: You can assign users as managers of a knowledge base.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration tasks for knowledge managers, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assign a knowledge base manager

You can assign users as managers of a knowledge base.

## Before you begin

Role required: knowledge\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Bases**.

2.  Select a knowledge base you manage.

3.  In the **Managers** field, click the unlock icon.

4.  Add one or more users.

5.  Click **Update**.

    After you save the knowledge base record, users selected as managers automatically receive the knowledge\_manager role if they do not have it already.


## What to do next

You can remove a knowledge base manager by removing that user from the **Managers** field. If the user is not a manager of any other knowledge base, the knowledge\_manager role is removed from that user.

**Parent Topic:**[Configuration tasks for knowledge managers](../concept/c_KnowledgeManager.md)

**Related topics**  


[Add a knowledge article to featured content](t_PinAnArticle.md)

[Define a knowledge article category](t_DefineAKnowledgeCategory.md)

