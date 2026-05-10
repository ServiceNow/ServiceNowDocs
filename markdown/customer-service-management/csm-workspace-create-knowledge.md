---
title: Create a knowledge article from a case
description: Create knowledge articles from customer service cases to save case information and make it available to others in a knowledge base.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using CSM Configurable Workspace in Customer Service Management, Manage cases, Use, Customer Service Management]
---

# Create a knowledge article from a case

Create knowledge articles from customer service cases to save case information and make it available to others in a knowledge base.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, workspace\_admin, admin

## About this task

When you create or edit a knowledge article in CSM Configurable Workspace, you can access the editing capabilities available with the [Knowledge Center article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-article-editor.md). Use the editing capabilities available with the article editor to format article content such as text, images, and media.

When creating a knowledge article, you can select a knowledge base and an article template and see a preview of the selected template. Then you can use the article editor in CSM Configurable Workspace to create the article.

**Note:** The **sn\_km\_center.glide.knowman.ece.enable** system property enables the Knowledge Center article editor within CSM Configurable Workspace. This property is set to true by default for zBoot customers and can be enabled by upgrade customers.

Before creating knowledge articles, the system administrator needs to [enable creation of articles from customer service cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/administer-create-article-from-case.md).

## Procedure

1.  Open a customer service case.

2.  Select **Create** &gt; **Create Knowledge**.

    The system displays an interceptor page.

3.  Select a knowledge base.

    After selecting a knowledge base, the system displays a list of the active templates.

4.  Select an article template.

5.  View the template preview and then select **Next**.

    The system displays the Knowledge Center article editor.

6.  Use the article editor to create your article.

    The article editor page includes three columns:

    -   Article information fields
    -   Article editor
    -   Article building blocks and settings
    For more information about using the Knowledge Center article editor to create your article, see [Generate and edit articles using the article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-edit-knowledge-article.md).

7.  Select **Save**.


