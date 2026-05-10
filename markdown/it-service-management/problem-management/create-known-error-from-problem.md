---
title: Create a known error article
description: Create known error articles as reference material. The known error articles document the root cause and the workaround of the problem to help with deflecting incidents.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Communicating the outcome of a problem, Problem Management, IT Service Management]
---

# Create a known error article

Create known error articles as reference material. The known error articles document the root cause and the workaround of the problem to help with deflecting incidents.

## Before you begin

Role required: admin, problem\_admin, problem\_coordinator, or problem\_manager

Activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) and the Problem Management Best Practice — Madrid — Knowledge Integration \(com.snc.best\_practice.problem.madrid.knowledge\) plugin.

## About this task

After you create a known error article from a problem, the article is saved in the knowledge base and maintained in the Knowledge Management application. The publishing and retirement processes for a knowledge article are controlled by workflows defined for the knowledge base that the article belongs to. For more information, see [Knowledge workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeWorkflows.md).

## Procedure

1.  Navigate to **All** &gt; **Problem** &gt; **Open**.

2.  Open the Problem record.

3.  Under **Related Links**, click **Create Known Error Article**.

    **Note:** The link appears when the **Primary Known Error article** field is empty under the **Analysis Information** tab on the Problem form.

4.  Click **Submit**.

    **Note:** To read the content of the article, click **View Article** under **Related Links**.

5.  On the form, fill in the fields.

    **Note:** Click **Search for Duplicates** to search for existing known error articles. The search is based on short description, category, and topic.

    For a description of the field values, see [Known error article form](../reference/known-error-article-form.md).


## What to do next

Click **Publish** to send the article for review and approval. Depending on the Knowledge base where the article is stored and the Knowledge Base access controls, this Known Error article may be available to search for users outside of the IT team to help with Incident deflection.

**Parent Topic:**[Communicating the outcome of a problem](../concept/communicate-outcome-of-problem.md)

