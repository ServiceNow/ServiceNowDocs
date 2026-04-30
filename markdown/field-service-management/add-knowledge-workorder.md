---
title: Add a knowledge article to a work order or work order task
description: Add additional information to complete tasks.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Add a knowledge article to a work order or work order task

Add additional information to complete tasks.

## Before you begin

To enable the search and to attach articles on the form, the system administrator must do the following:

-   Configure the work order and work order task forms to display the **Related Search Results** section on the forms.
-   In the **glide.knowman.attach.fields** property, add `work_notes` to the **Value** field. This enables the attaching of articles to the work notes.

Role required: wm\_initiator, wm\_qualifier, wm\_agent, wm\_manager, wm\_dispatcher, or admin

## About this task

As you enter a short description for a work order or work order task, a list of relevant knowledge articles is displayed that you can associate with the work order or work order task.

## Procedure

1.  Navigate to a work order or a work order task form.

2.  Click **Related Search Results**.

    A list of articles that match the text entered in the **Short Description** field are displayed.

3.  To preview, click the article.

4.  To attach an article,

    -   To attach the article you're previewing, click **Attach to Work Order**.
    -   To attach an article without previewing it, click **Attach** next to it in the list of suggested articles.
5.  Click **Update**.


## Result

The articles are added and appear under the **Attached Articles** tab.

**Parent Topic:**[Managing work orders and work order tasks](../concept/managing-work-orders.md)

**Related topics**  


[Knowledge properties](https://www.servicenow.com/docs/access?context=r_KnowledgeProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

