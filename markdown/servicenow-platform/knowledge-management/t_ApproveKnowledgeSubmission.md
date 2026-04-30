---
title: Create knowledge from incident or problem
description: Create a knowledge article, so the next time the issue comes up the resolution is easy to find.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create knowledge from incident or problem

Create a knowledge article, so the next time the issue comes up the resolution is easy to find.

## Before you begin

Role required: knowledge

## About this task

To create a knowledge article from an incident, see [Create a knowledge article from an incident](https://www.servicenow.com/docs/access?context=create-knowledge-incident&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

To create a knowledge article from problem, see [Create a known error article](https://www.servicenow.com/docs/access?context=create-known-error-from-problem&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

Depending on the value of the **glide.knowman.submission.workflow** property, knowledge created from an incident or problem may require additional approval. When this property is true, a submission record is created instead of a knowledge article. A user with the knowledge role must approve the submission to create a knowledge article.

## Procedure

1.  Open a resolved incident or problem.

2.  Select the **Knowledge** check box on the form.

    You may need to configure the form to include the **Languages** field. Click the form context menu icon \(![context menu icon](../image/ContextMenu.png)\) and navigate to **Configure** &gt; **Form layout**. Use slushbucket to add the Languages field.

3.  Close the incident or problem.

    A new draft knowledge article is created.

4.  If additional approval is required, navigate to **Knowledge** &gt; **Articles** &gt; **Open Submissions**.

5.  Select a submission record.

6.  Review the submission to ensure the content and settings are correct.

7.  Click **Create Article**.

    A new draft knowledge article is created. Articles created this way are added to the knowledge base specified in the property **glide.knowman.task\_kb**.


**Parent Topic:**[Creating and maintaining articles](../../../creating-and-maintaining-articles.md)

