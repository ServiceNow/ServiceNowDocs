---
title: Train the similarity solution for Demand Management to find similar demands
description: Train the Similar Demands solution definition is included within the Predictive Intelligence for PPM capability to find related demands when creating a demand.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Train the similarity solution for Demand Management to find similar demands

Train the Similar Demands solution definition is included within the Predictive Intelligence for PPM capability to find related demands when creating a demand.

## Before you begin

Confirm that the Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\), PPM Standard plugin \(com.snc.financial\_planning\_pmo\), and Predictive Intelligence for PPM plugin \(com.snc.ppm\_ml\) are activated. For more information about Predictive Intelligence, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Demands solution definition \(ml\_sn\_global\_global\_similar\_demands\).

3.  On the Similarity Definition form, verify the default field values for demands.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

4.  Select **Update &amp; Retrain**.

5.  Open the Similarity Definition form for the Similar Demands solution definition \(ml\_sn\_global\_global\_similar\_demands\).

6.  In the ML Solutions related list, view the training solution progress in the **Progress** column.

    **Note:** Alternatively, you can select the link for the solution in the **Active** column. On the ML Solution form, select the **Show training progress** related link to check the training solution progress.


## Result

When the solution is complete, the similar demands appear in the Similar demands section on the Demand form.

## What to do next

-   Review similarity examples: On the Similarity Definition form, in the ML Solutions related list, when **Progress** is 100%, in the **Active** column, select the link for the solution. On the ML Solution form, select the **Similarity Examples** related link to view the Similarity Examples list.
-   Update the similarity score threshold: On the ML Solution form, on the **Solution Statistics** tab, enter the required value in the **Similarity Score Threshold** field. Right-click the ML Solution form and select **Save**.
-   Test the prediction output for the records: On the ML Solution form, on the **Test solution** tab, enter your text in the **Short description** field and the maximum number of expected results in the **Top N** field, and then select **Run test**. The results above the similarity score threshold value are displayed.

**Parent Topic:**[Use Demand Management](../reference/r_UsingDemandManagement.md)

**Related topics**  


[Assess demands](../concept/c_AssessingDemands.md)

[Create a demand](t_CreatingDemands.md)

[View demands](t_ViewDemands.md)

[Add details to demands](../concept/c_EnhancingDemands.md)

[RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records for a demand](../concept/ridac-entries-for-demand.md)

[Reset a demand to Draft state](reset-demand-to-draft-state.md)

[Delete demands](t_DeletingDemands.md)

[Move and resize a demand](t_MoveAndResizeADemand.md)

[PPM PIWB template - Find similar demands](../../itbm-PI-workbench/task/ppm-piwb-demand.md)

[Identify similar records using Now Assist for Strategic Portfolio Management \(SPM\)](identify-similar-demands.md)

[Summarize demands with demand summarization skill](demand-summary-demand-classic.md)

[Associate AI systems with demands](associate-ai-systems-with-demands.md)

[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Predictive Intelligence for Demand Management](../concept/predictive-intelligence-for-demand.md)

[Create a demand](t_CreatingDemands.md)

