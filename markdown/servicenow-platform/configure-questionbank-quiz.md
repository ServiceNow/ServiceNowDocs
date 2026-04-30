---
title: Configure metric categories or metrics for a quiz using the question bank
description: Reuse question categories \(metric categories\) and questions \(metrics\) from the Question Bank module while creating or updating a quiz.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Add a metric category and metric in the question bank for quizzes, Use, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure metric categories or metrics for a quiz using the question bank

Reuse question categories \(metric categories\) and questions \(metrics\) from the **Question Bank** module while creating or updating a quiz.

## Before you begin

Role required: admin or assessment\_admin

## Procedure

1.  Navigate to **All** &gt; **Quizzes** &gt; **Quizzes**.

2.  Open a quiz definition.

3.  To add metric categories to a quiz from the question bank in Platform, perform the following steps.

    1.  In the Metric Categories related list, click **New Category from Bank**.

        The New Category from Bank dialog box is displayed with a list of all metric categories added in the question bank.

    2.  Select the required categories and click **Add Selected**.

        A copy of the metric category and the corresponding metric definitions is created in the Metric Categories related list.

4.  To add metrics to a quiz from the question bank in Platform, perform the following steps.

    1.  In the Metric Categories related list, open a metric category definition.

    2.  In the Assessment Metrics related list, click **New Metric from Bank**.

        The New Metric from Bank dialog box is displayed with a list of questions available in the question bank.

    3.  Select the required metrics and click **Add Selected**.

        A copy of the metric and the corresponding metric definitions is created in the Assessment Metrics related list of the category.

5.  To add a metric category to the question bank from a quiz in Platform, perform the following steps.

    1.  In the Metric Categories related list, open a metric category definition.

    2.  Click **Add to Question Bank**.

        A copy of the category is created along with its metrics and metric definitions in the question bank.

6.  To add a metric to the question bank from a quiz in Platform, perform the following steps.

    1.  In the Metric Categories related list, open a metric category definition.

    2.  In the Assessment Metrics related list, open the required metric definition.

    3.  Click **Add to Question Bank**.

        The Add to Question Bank dialog box is displayed.

    4.  In the **Choose a question bank to add this question/metric** field, select a metric category that you want to add this metric to, and click **OK**.

        A copy of the metric and the corresponding metric definitions is created for the selected category in the question bank.

7.  To add a metric category or metric to a quiz from the question bank in Quiz Designer, perform the following steps.

    1.  Open the quiz in Quiz Designer.

    2.  To add a metric category from the question bank, from the **Categories** tab in the left panel, drag the required category banner and drop in the **Design** tab.

    3.  To add a metric from the question bank, drag and drop the required metric from the **Questions** tab or the **Categories** tab.

    **Note:**

    -   When you drag and drop a metric category, all dependencies within the category are also added to the quiz.
    -   From the **Categories** tab, you can drag and drop an individual metric within a metric category.
    -   When you drag and drop a parent metric, all dependent questions are also added to the metric category.
    -   When you drag and drop a child metric, only the child question is added to the metric category.

**Parent Topic:**[Add a metric category and metric in the question bank for quizzes](add-questionbank-quiz.md)

