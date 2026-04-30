---
title: Define a knowledge article category
description: Each knowledge base has a hierarchy of categories that organizes the articles.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration tasks for knowledge managers, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a knowledge article category

Each knowledge base has a hierarchy of categories that organizes the articles.

## Before you begin

Role required: knowledge\_admin, knowledge\_manager, **CanContribute** access to the knowledge base

## About this task

Define a hierarchy for categories by creating parent-child relationships. Each hierarchy consists of a top-level category and a structure of subcategories, which are also named the child categories. The category hierarchy is saved in the **Full category** field in the Knowledge Category \[kb\_category\] table.

You can create and edit categories separately for each knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Select a knowledge base you manage.

3.  Create a top-level category.

    1.  In the Knowledge Categories related list, click **New**.

    2.  On the Knowledge Category form, fill in the fields.

<table id="table_zpb_v2d_hmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label for the category.The label appears as the name of the category.

</td></tr><tr><td>

Value

</td><td>

Value for the category you use when referencing the category in scripts.

</td></tr><tr><td>

Parent ID

</td><td>

Top-level component associated with the category.This field is automatically set to the top-level component ID.

</td></tr><tr><td>

Active

</td><td>

Option to enable the category.

</td></tr></tbody>
</table>    3.  Click **Submit**.

4.  Create a child category.

    1.  Expand an existing category and click **New** within the expanded section.

    2.  Fill in the [Knowledge Category form](t_DefineAKnowledgeCategory.md#table_zpb_v2d_hmb).

    3.  Click **Submit**.


## What to do next

In addition to using categories defined by a knowledge manager, knowledge contributors can add and edit categories when editing an article.

**Parent Topic:**[Configuration tasks for knowledge managers](../concept/c_KnowledgeManager.md)

**Related topics**  


[Add a knowledge article to featured content](t_PinAnArticle.md)

[Assign a knowledge base manager](t_AssignAKnowledgeBaseManager.md)

[Select a knowledge article category](t_SelectACategory.md)

