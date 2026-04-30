---
title: Train the similarity solution for Knowledge Management to find related articles
description: Train the Knowledge Similar Articles solution definition included within the Predictive Intelligence for Knowledge Management capability to find related knowledge articles when creating or viewing a knowledge article.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Train the similarity solution for Knowledge Management to find related articles

Train the Knowledge Similar Articles solution definition included within the Predictive Intelligence for Knowledge Management capability to find related knowledge articles when creating or viewing a knowledge article.

## Before you begin

Ensure that the Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\) and Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\) are activated.

Role required: admin

**Note:** This solution is only applicable to OOB \(Out of Box\) similarity solution and not to knowledge articles that are created manually.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Knowledge Similar Articles solution definition \(ml\_sn\_global\_knowledge\_similar\_articles\).

3.  On the Similarity Definition form, verify the default field values for knowledge articles.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    **Note:** If the application scope isn't set to Knowledge Management - Machine Learning, you cannot edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

4.  Click **Update &amp; Retrain**.

5.  Open the Similarity Definition form for the Knowledge Similar Articles solution definition \(ml\_sn\_global\_knowledge\_similar\_articles\).

6.  In the ML Solutions related list, view the training solution progress in the **Progress** column.

    When **Progress** is 100%, in the ML Solutions related list, you can include more useful related articles by reviewing the similarity examples based on the similarity score and updating the similarity score threshold value.

7.  Update the similarity score threshold.

    1.  In the **Active** column, click the link for the solution.

    2.  Review the similarity examples by clicking the **Similarity Examples** related link on the ML Solution form.

        For more information, see [Review solution similarity examples](https://www.servicenow.com/docs/access?context=review-similarity-examples&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    3.  In the Solution Statistics related list on the ML Solution form, enter the required value in the **Similarity Score Threshold** field, right-click the ML Solution form, and then click **Save**.

        For more information, see [Update your similarity score threshold](https://www.servicenow.com/docs/access?context=update-similarity-threshold&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).


## Result

When the solution is complete, the related knowledge articles appear in the Knowledge results section on the Knowledge form in the ServiceNow AI Platform, in the Related Articles section on the knowledge article view page in the Knowledge Management Service Portal, and in Agent assist when the **Similar Articles \(ML\)** option is selected.

**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

**Related topics**  


[Predictive Intelligence for Knowledge Management](../concept/predictive-intelligence-for-km.md)

[Knowledge Management Service Portal article view page features](../concept/knowledge-service-portal-view.md)

[Create a knowledge article](create-knowledge-article.md)

[Create a knowledge article in Agent Workspace](create-article-workspace.md)

[Using Now Mobile for Knowledge Management](../concept/mobile-experience-for-km.md)

