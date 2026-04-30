---
title: Request translations for missing languages in Agent Workspace
description: Request to translate a published knowledge article in available languages by creating a translation task in Agent Workspace.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request translations for missing languages in Agent Workspace

Request to translate a published knowledge article in available languages by creating a translation task in Agent Workspace.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated.
-   I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) is activated.

    **Note:** The 18N: Internationalization plugin \(com.glide.i18n\) activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

-   The **glide.knowman.translation.enable\_translation\_task** property is set to `true` in the ServiceNow AI Platform interface. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

Role required: agent\_workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Click **Lists** &gt; **Knowledge** &gt; **All Articles**.

3.  Click the link to a knowledge article for which you want to create a translation task.

4.  On the Knowledge form, click **Edit**.

5.  Click **Request translations**.

6.  In the Request translation dialog box, select one or more available languages in the Select languages list.

    If a language appears grayed out, a translation is already in progress or has been completed for that language. Some languages might not be available if the system administrator has configured only specific languages for the knowledge base in which the article is contained.

7.  Click **Submit**.


## Result

The translation task is created for the article in the selected languages and assigned to a group or user based on assignment rules, if configured.

**Related topics**  


[Create translation assignments for knowledge articles](create-translation-assignments.md)

[Translate a knowledge article from a translation task in Agent Workspace](translate-article-agent.md)

