---
title: Knowledge base setup guide for knowledge admins and managers
description: After basic Knowledge Management setup is completed, you can set up a knowledge base for users to create and publish knowledge articles.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge base setup guide for knowledge admins and managers

After basic Knowledge Management setup is completed, you can set up a knowledge base for users to create and publish knowledge articles.

Create multiple knowledge bases for different groups within your organization to share information within and between those groups. Create scoped knowledge bases to enable only application administrators to administer the knowledge bases and restrict unauthorized access to application-specific data.

Administrators create knowledge bases, and assign them to individual managers responsible for controlling the behavior and organization scheme of each knowledge base.

Each knowledge base contains knowledge articles that provide information for users, such as policy, release notes, or instructions for a task. Each knowledge base can also use a separate workflow for publishing and retiring articles.

## Requirements

Role required: knowledge\_administrator, knowledge\_manager, or admin.

## Before you begin

-   **Determine the following requirements for each knowledge base that you want to set up:**
    -   Whether to create a scoped knowledge base? For more information, see [Scoped knowledge bases](../concept/scoped-knowledge-base-administration.md).
    -   Who are the knowledge base managers that are responsible for approving articles?
    -   Who are the users and contributors for that knowledge base? Access for these users is defined through user criteria.
    -   What are the categories to be used to classify articles? Will users be able to create categories?
    -   Will users of the knowledge base be able to create new content?

## What to do

-   **Set up the knowledge base**
    1.  Create the [knowledge base](../task/create-a-knowledgebase.md).
    2.  Set up which users can read, create, or edit knowledge articles by [selecting user criteria](../task/t_SelectUserCriteria.md) for the knowledge base.
    3.  Define the approval process for articles using [workflows](r_KnowledgeWorkflows.md).
    4.  Define the [knowledge categories](../task/t_DefineAKnowledgeCategory.md) that are needed for organizing articles in the knowledge base.
    5.  If you want a [custom knowledge homepage](../task/t_CreateACustomKnowledgeHomepage.md), ask your ServiceNow administrator to create it.

## Next steps

Let users in your organization know that they can start creating and searching articles in the knowledge base. For details, refer users to the [Knowledge Management guide for users](get-started-knowledge-end-users.md).

If you have the knowledge\_manager role, there are many other tasks that you can perform to maintain the knowledge base. You can pin articles so they are featured prominently in the search results and on landing pages. You can also assign other users as managers of a knowledge base. For details, see [Configuration tasks for knowledge managers](../concept/c_KnowledgeManager.md).

**Parent Topic:**[Configuring Knowledge Management](../../../configuring-knowledge-management.md)

