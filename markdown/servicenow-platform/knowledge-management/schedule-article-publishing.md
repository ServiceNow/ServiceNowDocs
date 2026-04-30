---
title: Schedule a knowledge article for publishing
description: Set a specific time and day for a knowledge article to be published automatically.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Schedule a knowledge article for publishing

Set a specific time and day for a knowledge article to be published automatically.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article you want to schedule for publishing.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated. For more information, see [Activate the Knowledge Management Advanced plugin](activate-knowledge-advanced-plugin.md).
-   The article versioning feature is enabled. For more information, see [Article versioning](../concept/article-versioning.md).

Role required: knowledge

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** and click **Unpublished**.

2.  Select an article link.

3.  In the **Scheduled publish date** field, click the select date and time icon ![Select date and time icon](../image/date-time.png).

    You may need to configure the knowledge block form to include the **Scheduled publish date** field. Click the form context menu icon \(![context menu](../image/ContextMenu.png)\) and navigate to **Configure** &gt; **Form Layout**. Use slushbucket to add the Scheduled publish date field.

    **Important:** You must set the **Scheduled publish date** at least 24 hours from the current date. To publish the article earlier than 24 hours, click **Publish article** available in the form.

4.  Select any future date from the calendar.

5.  In the **Time** field, enter a time in the format hh:mm:ss.

6.  Select the save \(enter\) icon ![Save enter icon](../image/save-km.png).

7.  Select **Publish** to enable the publishing workflow.

    The article is available in the All list. Go to **Knowledge** &gt; **Articles** &gt; **All**.

    **Tip:** If you want to cancel an article's scheduled publication and move the article back to the Draft state, click **Recall**.


## Result

The knowledge article is published on the scheduled publish date depending on the following workflow settings of its knowledge base:

-   If the knowledge base workflow is set to **Knowledge - Instant Publish**, the knowledge article is automatically published on the scheduled publish date. The **Workflow** field on the Knowledge form of the article is updated to **Scheduled for publish**.
-   If the knowledge base workflow is set to **Knowledge - Approval Publish**, the knowledge article is published on approval completion. The **Workflow** field on the Knowledge form of the article is updated to **Review**.

    The approval completion affects the scheduled publishing as follows:

    -   If the approvals are completed before the scheduled publish date, the **Workflow** field on the Knowledge form of the article is updated to **Scheduled for publish** and the article is published on the scheduled publish date.
    -   If the approvals are completed after the scheduled publish date, the article is published immediately on the approval completion.

**Parent Topic:**[Creating and maintaining articles](../../../creating-and-maintaining-articles.md)

**Related topics**  


[Edit a knowledge article](edit-knowledge-article.md)

