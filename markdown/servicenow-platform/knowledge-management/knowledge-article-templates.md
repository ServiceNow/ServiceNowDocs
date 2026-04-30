---
title: Knowledge article templates
description: Article templates have pre-defined fields structured in a specific order. These templates help create a consistent structure for knowledge articles.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge article templates

Article templates have pre-defined fields structured in a specific order. These templates help create a consistent structure for knowledge articles.

Using the Knowledge Article Templates feature, as a knowledge administrator \(a user with knowledge\_admin role\), you can create article templates, add or customize fields in a template, and activate or deactivate a template.

As a security administrator \(a user with security\_admin role\), you can configure field-level security in any template to make it visible to specific users.

As an author, you can create articles using pre-defined article templates or any newly created article templates.

## Pre-defined knowledge article templates

Use either the standard template or one of the pre-defined How To, What Is, FAQ or KCS article templates.

**Note:**

When you upgrade Knowledge Management to Kingston or later releases, all the existing articles from the earlier version automatically use the standard template of the upgraded version. For example, if you upgrade Knowledge Management from Jakarta to Kingston, all existing articles use the standard template available in the Kingston version.

All pre-defined templates are inactive by default. If you do not activate a template, the articles automatically use the standard template. As a knowledge admin, you can activate a template by navigating to **Knowledge** &gt; **Administration** &gt; **Article Templates**. Then in the article template list, set the **Active** field to true for one or more templates you would like to activate.

Templates are associated with knowledge bases. Only templates which are active and associated with a knowledge base are shown.

The template structure is stored in kb\_article\_template while the fields for each template are stored in kb\_article\_template\_definition. For creating and manipulating templates navigate to **Knowledge** &gt; **Administration** &gt; **Article Templates**.

The table below lists the fields available in each template and the name of the template table.

<table id="table_mqs_grq_lbb"><thead><tr><th>

Template name

</th><th>

Template fields

</th><th>

Maps to table

</th><th>

SEO Description Tag

</th></tr></thead><tbody><tr><td>

FAQ

</td><td>

-   Question
-   Answer

</td><td>

FAQ \[kb\_template\_faq\]

</td><td>

Question

</td></tr><tr><td>

How To

</td><td>

-   Introduction
-   Instructions

</td><td>

How To \[kb\_template\_how\_to\]

</td><td>

Introduction

</td></tr><tr><td>

What Is

</td><td>

-   Introduction
-   Explanation

</td><td>

What Is \[kb\_template\_what\_is\]

</td><td>

Introduction

</td></tr><tr><td>

KCS Article

</td><td>

-   Issue
-   Environment
-   Cause
-   Resolution

</td><td>

KCS Article \[kb\_template\_kcs\_article\]

</td><td>

Issue

</td></tr><tr><td>

Standard

</td><td>

Text

</td><td>

kb\_knowledge

</td><td>

Text

</td></tr></tbody>
</table>## Activating knowledge article templates

The Knowledge Article Templates feature is activated with the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) plugin. After the feature is activated, when creating an article, option to choose a template for the article appears. For details, see [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md).

## Deactivating knowledge article templates

You cannot delete an article template because article templates have an associated child table. Deleting a template would also require deleting the child table. Due to the limitations on dropping tables, article templates and template columns are explicitly made non-deletable. Instead, you can disable the Knowledge Article Templates feature by clearing the **Active** check box on the Article Template form.

**Note:** The Standard template is available by default and can’t be made inactive.

**Parent Topic:**[Knowledge Management](knowledge-management.md)

**Related topics**  


[Configure knowledge article templates](configure-knowledge-article-templates.md)

