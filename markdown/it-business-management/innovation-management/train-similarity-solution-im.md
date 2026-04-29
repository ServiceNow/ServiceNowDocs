---
title: Train the similarity solution for Innovation Management to find similar ideas
description: Train the Similar Ideas solution definition included within the Predictive Intelligence for Ideation capability to find related ideas when submitting an idea or viewing ideas in the Idea Portal.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing ideas using Innovation Management, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Train the similarity solution for Innovation Management to find similar ideas

Train the Similar Ideas solution definition included within the Predictive Intelligence for Ideation capability to find related ideas when submitting an idea or viewing ideas in the Idea Portal.

## Before you begin

Ensure that the Predictive Intelligence plugin \(com.glide.platform\_ml\), PPM Standard plugin \(com.snc.financial\_planning\_pmo\), and Predictive Intelligence for Ideation plugin \(com.snc.innovation\_management\_ml\) are activated. For more information about Predictive Intelligence, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Ideas solution definition \(ml\_sn\_global\_similar\_ideas\).

3.  On the Similarity Definition form, verify the default field values for ideas.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

4.  Click **Update &amp; Retrain**.

5.  Open the Similarity Definition form for the Similar Ideas solution definition \(ml\_sn\_global\_similar\_ideas\).

6.  In the ML Solutions related list, view the training solution progress in the **Progress** column.

    **Note:** Alternatively, you can click the link for the solution in the **Active** column. On the ML Solution form, click the **Show training progress** related link to check the training solution progress.


## Result

When the solution is complete, the similar ideas appear in the Related Ideas section on the Create an Idea form and Related Ideas section on the Ideas page in the Idea Portal.

## What to do next

-   Review similarity examples: On the Similarity Definition form, in the ML Solutions related list, when **Progress** is 100%, in the **Active** column, click the link for the solution. On the ML Solution form, click the **Similarity Examples** related link to view the Similarity Examples list.
-   Update the similarity score threshold: On the ML Solution form, on the **Solution Statistics** tab, enter the required value in the **Similarity Score Threshold** field. Right-click the ML Solution form and click **Save**.
-   Test the prediction output for the records: On the ML Solution form, on the **Test solution** tab, enter your text in the **Short description** field and the maximum number of expected results in the **Top N** field, and then click **Run test**. The results above the similarity score threshold value are displayed.

**Parent Topic:**[Managing ideas using Innovation Management](../concept/using-innovation-management.md)

**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Predictive Intelligence for Innovation Management](../concept/predictive-intelligence-for-innovation.md)

[Submit an idea](submit-idea-in-idea-portal.md)

