---
title: Train the similarity solution for Project Management to find similar projects
description: Train the Similar Projects solution definition included within the Predictive Intelligence for PPM capability to find related projects when defining a project.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Train the similarity solution for Project Management to find similar projects

Train the Similar Projects solution definition included within the Predictive Intelligence for PPM capability to find related projects when defining a project.

## Before you begin

Ensure that the Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\), PPM Standard plugin \(com.snc.financial\_planning\_pmo\), and Predictive Intelligence for PPM plugin \(com.snc.ppm\_ml\) are activated. For more information about Predictive Intelligence, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Projects solution definition \(ml\_sn\_global\_global\_similar\_projects\).

3.  On the Similarity Definition form, verify the default field values for projects.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

4.  Click **Update &amp; Retrain**.

5.  Open the Similarity Definition form for the Similar Projects solution definition \(ml\_sn\_global\_global\_similar\_projects\).

6.  In the ML Solutions related list, view the training solution progress in the **Progress** column.

    **Note:** Alternatively, you can click the link for the solution in the **Active** column. On the ML Solution form, click the **Show training progress** related link to check the training solution progress.


## Result

When the solution is complete, the similar projects appear in the Similar projects section on the Project form.

## What to do next

-   Review similarity examples: On the Similarity Definition form, in the ML Solutions related list, when **Progress** is 100%, in the **Active** column, click the link for the solution. On the ML Solution form, click the **Similarity Examples** related link to view the Similarity Examples list.
-   Update the similarity score threshold: On the ML Solution form, on the **Solution Statistics** tab, enter the required value in the **Similarity Score Threshold** field. Right-click the ML Solution form and click **Save**.
-   Test the prediction output for the records: On the ML Solution form, on the **Test solution** tab, enter your text in the **Short description** field and the maximum number of expected results in the **Top N** field, and then click **Run test**. The results above the similarity score threshold value are displayed.

**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Predictive Intelligence for Project Management](../concept/predictive-intelligence-for-project.md)

[Starting a project](t_CreateAProject.md)

