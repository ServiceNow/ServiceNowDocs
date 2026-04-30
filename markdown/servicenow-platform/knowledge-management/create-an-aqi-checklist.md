---
title: Create an AQI checklist
description: Create a checklist of questions that reviewers can use to evaluate the quality of knowledge articles.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Article Quality Index, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an AQI checklist

Create a checklist of questions that reviewers can use to evaluate the quality of knowledge articles.

## Before you begin

Role required: knowledge\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Article Quality Index** &gt; **AQI checklists**, and click **New**.

2.  Fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Checklist|Name for the checklist.|
    |Description|Description for the checklist.|

3.  Right-click the form header and click **Save**.

4.  In the **Checklist Questions** related list, add questions to the checklist.

    Add questions and adjust the weight of the questions until the combined weight of all questions is equal to 100. The weight defines the score that is added to the total AQI review score of the article when the answer for that question is set to **true**. The maximum score that can be applied to an article in an AQI review is 100.

    **Note:** The default AQI pass score is 70. You can change the pass score in the [Article Quality Index properties](../reference/r_KnowledgeProperties.md#).

    To add a question:

    1.  Click **New**.

    2.  Fill in the following fields:

<table id="table_qt1_txc_rbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Text for the question to evaluate articles.

</td></tr><tr><td>

Description

</td><td>

Short description for the question.

</td></tr><tr><td>

Order

</td><td>

Value for the display order of questions in the checklist.The lower the value in the **Order** field, the higher the question displays in the checklist.

 **Note:** Before you assign a value for the display order, think about how many questions you would create for the checklist. For example, if you have five questions in a checklist, you can assign the value in increments of 20. This ensures that you have enough values to assign if you add questions to the checklist later.

</td></tr><tr><td>

Weight

</td><td>

A value for the question to score the article quality. This value is added to the AQI score when the answer for the question is set to **true**.**Note:**

-   The combined weight of all questions cannot exceed 100.
-   The sum of weights of all questions in a checklist must be equal to 100 to be assigned to a knowledge base.


</td></tr></tbody>
</table>    3.  Click **Submit**.

5.  After you finish adding questions to the checklist, click **Update** on the AQI Checklist form.


## What to do next

After you create a checklist, [assign it to a knowledge base](assign-an-aqi-checklist-to-a-knowledgebase.md).

